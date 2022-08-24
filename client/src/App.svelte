<script>
  import Header from "./lib/Header.svelte";
  import Body from "./lib/Body.svelte";
  import PannelloComandi from "./lib/PannelloComandi.svelte";
  import LogWindow from "./lib/LogWindow.svelte";
  import Bottone from "./lib/Bottone.svelte";
</script>

<main>
  <Header />
  <Body>
    <LogWindow />
    <PannelloComandi>
      <Bottone titolo="Start" actionType="start"/>
      <Bottone titolo="Stop" actionType="stop"/>
      <Bottone titolo="Restart" actionType="restart"/>
      <Bottone titolo="Kill" actionType="kill"/>
    </PannelloComandi>
  </Body>
</main>

<style>
</style>
