<script>
  import Button from "./Button.svelte";
  import Toggle from "./Toggle.svelte";
  import Menu from "./Menu.svelte";
  export let name;
  let dog;
</script>

<main>
	<h1>moller design</h1>
	soon™<br>
  <Menu bind:on={dog}>hello, {name}!</Menu>
  Dog?
  <Toggle bind:on={dog} />
  <br />
  {#if dog}
    <Button>dog</Button>
  {/if}
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
