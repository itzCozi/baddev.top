<script lang="ts">
  interface Props {
    className?: string | undefined;
    href: string;
    text: string;
  }

  let { className = "", href, text }: Props = $props();
</script>

<li class={`flex flex-row gap-2 ${className}`}>
  <a
    {href}
    class="w-full"
    target="_blank">{text}</a>
</li>
