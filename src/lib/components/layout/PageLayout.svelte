<script lang="ts">
  interface Props {
    children?: import("svelte").Snippet;
  }

  let { children }: Props = $props();
</script>

<div class="flex items-center justify-center min-h-screen p-4">
  <div class="mx-auto flex flex-col gap-2 max-w-xs">
    {@render children?.()}
  </div>
</div>
