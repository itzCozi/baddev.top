<script lang="ts">
  import PageLayout from "$lib/layout/PageLayout.svelte";
  import ListItem from "$lib/layout/ListItem.svelte";
  import AccentButton from "$lib/buttons/AccentButton.svelte";
</script>

<PageLayout>
  <h1 class="text-3xl mb-3 flex gap-3 text-center items-center justify-center font-semibold">
    <a
      href="https://profile.codersrank.io/user/itzcozi"
      title="Coders Rank'"
      class="hover:bg-transparent hover:text-type-emphasized text-type-emphasized">BadDev</a>
  </h1>

  <p class="text-sm mb-2">
    Currently using <a
      class="font-semibold hover:bg-transparent hover:text-type-primary text-type-primary"
      href="https://neverlose.cc">NeverLose</a>
    in
    <a
      class="font-semibold hover:bg-transparent hover:text-type-primary text-type-primary"
      href="https://www.counter-strike.net/cs2">CS2</a> for HvH.
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
    <AccentButton
      title="Github"
      href="https://github.com/itzCozi">Github</AccentButton>
    <AccentButton
      title="Discord"
      href="https://discord.com/invite/mxhcENzG2j">Discord</AccentButton>
  </div>
</PageLayout>
