<script lang="ts">
  interface Props {
    className?: string | undefined;
    href: string;
    text: string;
  }

  let { className = "", href, text }: Props = $props();
</script>

<li class={`list-item ${className}`}>
  <a
    {href}
    target="_blank">{text}</a>
</li>
