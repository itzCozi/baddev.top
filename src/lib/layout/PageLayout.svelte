<script lang="ts">
  interface Props {
    children?: import("svelte").Snippet;
  }

  let { children }: Props = $props();
</script>

<div class="flex items-center justify-center p-4 min-h-screen">
  <div class="mx-auto w-[20rem] h-full border border-mono-divider p-4">
    {@render children?.()}
  </div>
</div>
