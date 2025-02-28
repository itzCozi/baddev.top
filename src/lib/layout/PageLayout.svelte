<script lang="ts">
  import { writable } from "svelte/store";
  interface Props {
    children?: import("svelte").Snippet;
  }

  let { children }: Props = $props();
  const store = writable(".");
  const countryStore = writable(".");
  const imageLoaded = writable(false);

  let dotCount = 1;
  const interval = setInterval(() => {
    store.set(".".repeat(dotCount));
    countryStore.set(".".repeat(dotCount));
    dotCount = (dotCount % 3) + 1;
  }, 500);

  fetch("https://api64.ipify.org?format=json")
    .then((res) => res.json())
    .then((data) => {
      clearInterval(interval);
      const ip = data.ip;
      return fetch(`https://ipapi.co/${ip}/json/`);
    })
    .then((res) => res.json())
    .then((data) => {
      const country = data.country_code;
      store.set(data.ip);
      countryStore.set(country);
      setTimeout(() => {
        imageLoaded.set(true);
      }, 1000); // Delay of 1 second
    });
</script>

<div class="flex flex-col justify-center p-4 min-h-screen relative">
  <div class="mx-auto w-[25rem] h-full border border-mono-divider p-4">
    {@render children?.()}
  </div>
  <p class="text-sm absolute bottom-2 left-2">
    Accessed by <span class="font-semibold">{$store}</span>
    {#if $countryStore && $imageLoaded}
      from
      <img
        src={`https://flagsapi.com/${$countryStore}/flat/24.png`}
        alt="Country Flag"
        class="inline-block ml-1" />
    {/if}
  </p>
</div>
