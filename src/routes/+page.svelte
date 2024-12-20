<script lang="ts">
  import PageLayout from "$lib/layout/PageLayout.svelte";
  import ListItem from "$lib/layout/ListItem.svelte";
  import Button from "$lib/buttons/Button.svelte";
  import { writable } from "svelte/store";
  import { goto } from "$app/navigation";

  const activeTab = writable("radio");
</script>

<PageLayout>
  <h1 class="text-3xl text-type-emphasized mb-4 flex gap-3 text-center items-center justify-center font-semibold">
    <a
      href="/"
      title="Home"
      class="hover:bg-transparent">
      <img
        src="/icon.png"
        loading="lazy"
        alt="Icon"
        class="h-14 w-auto hover:scale-105 duration-200 ease-in-out cursor-pointer" />
    </a> Radio
  </h1>

  <!-- Jerry rigged so the height stays constant during tab switches  -->
  <span class="flex flex-row gap-2 border-x border-t border-b-0 border-mono-divider px-2 w-fit">
    <button
      on:click={() => activeTab.set("radio")}
      class={`${$activeTab === "radio" ? "font-bold" : ""}`}>
      Radio
    </button>
    <div class="border border-r border-type-dimmed/65 my-1"></div>
    <button
      on:click={() => activeTab.set("artists")}
      class={`${$activeTab === "artists" ? "font-bold" : ""}`}>
      Artists
    </button>
  </span>

  <div class="border border-mono-divider mb-4 p-2 md:h-[705px]">
    {#if $activeTab === "radio"}
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
          href="https://www.youtube.com/@boilerroom"
          text="Boiler Room" />
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
          href="https://www.youtube.com/@idroomparis"
          text="ID*ROOM" />
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
          href="https://www.youtube.com/@SelectedBase"
          text="Selected." />
        <ListItem
          href="https://www.youtube.com/@RAWCUTSTV"
          text="RAW CUTS" />
      </ul>
    {/if}

    {#if $activeTab === "artists"}
      <ul>
        <ListItem
          href="https://soundcloud.com/jj-darragh"
          text="JJ Darragh" />
        <ListItem
          href="https://www.youtube.com/@davidloehlein"
          text="David Löhlein" />
        <ListItem
          href="https://www.youtube.com/@youna_kr"
          text="YOUNA" />
        <ListItem
          href="https://www.youtube.com/@ColinBenders"
          text="Colin Benders" />
        <ListItem
          href="https://www.youtube.com/@Linex-PanicRoom"
          text="Linex Panic Room" />
        <ListItem
          href="https://www.youtube.com/@chrisluno"
          text="Chris Luno" />
        <ListItem
          href="https://www.youtube.com/@BLONDISH"
          text="BLOND:ISH" />
        <ListItem
          href="https://www.youtube.com/@jorisvoorndj"
          text="Joris Voorn" />
        <ListItem
          href="https://www.youtube.com/@guidlle"
          text="guidlle" />
        <ListItem
          href="https://www.youtube.com/@Stlndrms"
          text="STLNDRMS" />
        <ListItem
          href="https://www.youtube.com/@JayHosking"
          text="Jay Hosking" />
      </ul>
    {/if}
  </div>

  <div class="flex justify-between items-center">
    <Button
      title="About"
      href="/about">About</Button>
  </div>
</PageLayout>
