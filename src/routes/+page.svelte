<script lang="ts">
  import PageLayout from "$lib/layout/PageLayout.svelte";
  import ListItem from "$lib/layout/ListItem.svelte";
  import Button from "$lib/buttons/Button.svelte";
  import { writable } from "svelte/store";
</script>

<PageLayout>
  <h1 class="text-3xl mb-3 flex gap-3 text-center items-center justify-center font-semibold">
    <a
      href="https://profile.codersrank.io/user/itzcozi"
      title="Coders Rank'"
      class="hover:bg-transparent hover:text-type-emphasized text-type-emphasized">BadDev</a>
  </h1>

  <p class="text-sm mb-2">
    Currently using <span class="font-semibold">NeverLose</span> in <span class="font-semibold">CS2</span> for HvH.
  </p>

  <div class="border border-mono-divider mb-4 p-2">
      <ul>
        <ListItem
          href="https://cozi.lol"
          text="BadDeveloper (software)" />
        <ListItem
          href="https://manjar-o.cc"
          text="[ManJar-O] DJ" />
        <ListItem
          href="https://wyzie.ru"
          text="The Wyzie Toolset" />
        <ListItem
          href="https://github.com/sussy-code"
          text="Dev of sudo-flix" />
      </ul>
  </div>

  <div class="flex justify-between items-center">
    <Button
      title="Github"
      href="https://github.com/itzCozi">Github</Button>
    <Button
      title="Discord"
      href="https://discord.com/invite/mxhcENzG2j">Discord</Button>
  </div>
</PageLayout>
