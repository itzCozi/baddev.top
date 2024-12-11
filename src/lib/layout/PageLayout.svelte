<script lang="ts">
  interface Props {
    children?: import("svelte").Snippet;
  }

  let { children }: Props = $props();
</script>

<div class="flex items-center justify-center p-4 min-h-screen">
  <div class="mx-auto flex flex-col gap-2 max-w-xs border-mono-divider border h-full p-4">
    {@render children?.()}
  </div>
</div>
