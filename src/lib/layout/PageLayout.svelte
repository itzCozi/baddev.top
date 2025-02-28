<script lang="ts">
  import { writable } from "svelte/store";
  interface Props {
    children?: import("svelte").Snippet;
  }

  let { children }: Props = $props();
  const store = writable(".");

  let dotCount = 1;
  const interval = setInterval(() => {
    store.set(".".repeat(dotCount));
    dotCount = (dotCount % 3) + 1;
  }, 5);

  fetch("https://api64.ipify.org?format=json")
    .then((res) => res.json())
    .then((data) => {
      clearInterval(interval);
      const ip = data.ip;
      store.set(ip);
    });
</script>

<div class="flex flex-col justify-center p-4 min-h-screen relative">
  <div class="mx-auto w-[25rem] h-full border border-mono-divider p-4">
    {@render children?.()}
  </div>
  <p class="text-sm absolute bottom-2 left-2">
    Accessed from <span class="font-semibold">{$store}</span>
  </p>
</div>
