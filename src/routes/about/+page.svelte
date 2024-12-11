<script lang="ts">
  import BorderButton from "$lib/components/buttons/BorderButton.svelte";
  import PageLayout from "$lib/components/layout/PageLayout.svelte";
  import Paragraph from "$lib/components/type/Paragraph.svelte";
  import Divider from "$lib/components/type/Divider.svelte";
</script>

<PageLayout>
  <h2 class="text-3xl text-type-emphasized flex gap-3 text-center items-center justify-center">
    About 365
  </h2>
  <Paragraph className="mt-3 mb-1">
    365 Radio is a collection of "radio stations" that stream and post mostly on YouTube. These
    channels mostly consist of DJ sets and other related content. Some of these have a strange
    twist, like DJing in the back of a kitchen, in a bathroom, or in an elevator. Only the best
    promoters/radio stations are included in this list. We love feedback, so if you have any
    suggestions, please let us know.
  </Paragraph>
  <BorderButton
    title="Email"
    onClick={() => window.open("mailto:dev@wyzie.ru")}
    className="w-full py-2 rounded-md">
    Email Us
  </BorderButton>
  <Divider />
  <div class="flex justify-between items-center">
    <a
      href="/"
      title="Home">Home</a>
    <a
      href="https://github.com/itzcozi/365"
      title="Source code">Source code</a>
  </div>
</PageLayout>
