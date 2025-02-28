<script lang="ts">
  import { writable, derived } from "svelte/store";
  import { onMount } from "svelte";

  interface Props {
    children?: import("svelte").Snippet;
  }

  let { children }: Props = $props();
  const store = writable("");
  const countryStore = writable("");

  const truncatedStore = derived(store, ($store) => {
    return $store.length > 18 ? $store.slice(0, 18) + "..." : $store;
  });

  let dotCount = 1;
  const interval = setInterval(() => {
    store.set(".".repeat(dotCount));
    countryStore.set(".".repeat(dotCount));
    dotCount = (dotCount % 4) + 1;
  }, 100);

  const timeout = setTimeout(() => {
    clearInterval(interval);
    store.set("Error");
    countryStore.set("Error");
  }, 10000); // 10 seconds timeout

  onMount(() => {
    fetch("https://api64.ipify.org?format=json")
      .then((res) => res.json())
      .then((data) => {
        clearInterval(interval);
        clearTimeout(timeout);
        const ip = data.ip;
        return fetch(`https://ipapi.co/${ip}/json/`);
      })
      .then((res) => res.json())
      .then((data) => {
        const country = data.country_code;
        store.set(data.ip);
        countryStore.set(country);
      })
      .catch((error) => {
        console.error("Error fetching IP or country data:", error);
        clearInterval(interval);
        clearTimeout(timeout);
        store.set("Unknown");
        countryStore.set("Unknown");
      });
  });
</script>

<div class="flex flex-col justify-center p-4 min-h-screen relative">
  <div class="mx-auto w-[23rem] h-full border border-mono-divider p-4">
    {@render children?.()}
  </div>
  <p class="text-sm absolute bottom-2 left-2">
    Accessed by <span
      class="font-semibold"
      title={$store}>{$truncatedStore}</span>
    {#if $countryStore}
      from
      <img
        src={`https://flagsapi.com/${$countryStore}/flat/24.png`}
        alt="Country Flag"
        class="inline-block" />
    {/if}
  </p>
</div>
