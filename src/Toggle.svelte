<script>
  export let on = false;
</script>

<button class:on on:click={() => (on = !on)}
  >{#if on}
    ✔
  {:else}
    ✖
  {/if}</button
>

<style>
  button {
    border-color: rgb(50, 50, 50);
    background: rgb(31, 31, 31);
    color: white;
    font-family: monospace;
    cursor: pointer;
    box-shadow: 5px 5px 0 rgb(31, 31, 31);
    transition: box-shadow 0.1s, transform 0.1s;
  }
  button:active {
    background: rgb(31, 31, 31);
  }
  :not(.on) {
    color: red;
  }
  .on {
    color: greenyellow;
    transform: translateX(5px) translateY(5px);
    box-shadow: 0 0 0 rgb(31, 31, 31);
  }
</style>
