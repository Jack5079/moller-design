<script lang="ts">
  export let on: boolean = false;
  import Button from "./Button.svelte";
</script>

<nav class:on>
  <header>
    {document.title}
    <Button on:click={() => (on = false)}>✖</Button>
  </header>
  <slot />
</nav>

<style>
  nav {
    text-align: left;

    width: 100vw;
    max-width: 200px;
    font-family: monospace;
    color: white;
    background: rgb(100, 100, 100);
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    transition: left 0.5s;
    z-index: 50;
  }
  header {
    background: rgb(50, 50, 50);
  }
  nav::before {
    width: 100vw;
    max-width: 200px;
    content: "";
    position: fixed;
    top: 0;
    bottom: 0;
    background: rgb(31, 31, 31);
    z-index: -1;
    left: 0;
    transition: left 0.5s 0.1s;
  }
  :not(.on),
  nav:not(.on)::before {
    left: -200px;
  }
</style>
