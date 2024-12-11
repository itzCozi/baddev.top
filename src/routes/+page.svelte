<script lang="ts">
  import Divider from "$lib/type/Divider.svelte";
  import ListItem from "$lib/layout/ListItem.svelte";
  import PageLayout from "$lib/layout/PageLayout.svelte";
  import Button from "$lib/buttons/Button.svelte";
</script>

<PageLayout>
  <h3
    class="text-3xl text-type-emphasized mb-3 flex gap-3 text-center items-center justify-center font-semibold">
    <img
      src="/icon.png"
      alt="Icon"
      class="h-14 w-auto" /> Radio
  </h3>
  <ul>
    <ListItem
      href="https://www.youtube.com/@hoer.berlin"
      text="Hoer Berlin" />
    <ListItem
      href="https://www.youtube.com/@yoyakurecordstore"
      text="Yoyaku Record Store" />
    <ListItem
      href="https://www.youtube.com/@BEATTVOfficial"
      text="BE-AT.tv" />
    <ListItem
      href="https://www.youtube.com/@lethimcookradio"
      text="Let Him Cook Radio" />
    <ListItem
      href="https://www.youtube.com/@bookclubradio"
      text="Book Club Radio" />
    <ListItem
      href="https://www.youtube.com/@stoorlab"
      text="STOOR" />
    <ListItem
      href="https://www.youtube.com/@Cercle"
      text="Cercle" />
    <ListItem
      href="https://www.youtube.com/@MISSIONLONDON_"
      text="MISSION LONDON" />
    <ListItem
      href="https://www.youtube.com/@Mixmag"
      text="Mixmag" />
    <ListItem
      href="https://www.youtube.com/@soireeelive"
      text="soirée live" />
    <ListItem
      href="https://www.youtube.com/@blackhouseradio"
      text="Black House Radio" />
    <ListItem
      href="https://www.youtube.com/@clockfactorybristol"
      text="Clock Factory" />
    <ListItem
      href="https://www.youtube.com/@radioradiofm"
      text="RRFM" />
    <ListItem
      href="https://www.youtube.com/@DJsounds"
      text="DJsounds" />
    <ListItem
      href="https://www.youtube.com/@FutureIntel"
      text="Future Intel" />
    <ListItem
      href="https://www.youtube.com/@timelessmusicofc"
      text="Time:Code" />
    <ListItem
      href="https://www.youtube.com/@KioskRadio"
      text="Kiosk Radio" />
    <ListItem
      href="https://www.youtube.com/@RadioRea"
      text="Radio Rea" />
    <ListItem
      href="https://www.youtube.com/@TheLotRadio"
      text="The Lot Radio" />
    <ListItem
      href="https://www.youtube.com/@KINDREDEVERYTHING"
      text="KINDRED" />
    <ListItem
      href="https://www.youtube.com/@KeepHush"
      text="Keep Hush" />
    <ListItem
      href="https://www.youtube.com/@detroitclassicgallery7108"
      text="Detroit Classic Gallery" />
    <ListItem
      href="https://www.youtube.com/@CollectRadio"
      text="Collect Radio" />
    <ListItem
      href="https://www.youtube.com/@hardwax_official"
      text="Hardwax" />
    <ListItem
      href="https://www.youtube.com/@RAWCUTSTV"
      text="RAW CUTS" />
    <ListItem
      href="https://www.youtube.com/@davidloehlein"
      text="David Löhlein" />
  </ul>
  <Divider />
  <div class="flex items-center justify-center">
    <Button
      title="About"
      href="/about">
      About
    </Button>
  </div>
</PageLayout>
