<button on:click on:dblclick on:focus on:blur on:contextmenu><slot /></button>

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
  button:hover {
    transform: translateX(3px) translateY(3px);
    box-shadow: 2px 2px 0 rgb(31, 31, 31);
  }
  button:focus {
    border-color: rgb(100, 100, 100);
  }
  button:active {
    background: rgb(31, 31, 31);
    transform: translateX(5px) translateY(5px);
    box-shadow: 0 0 0 rgb(31, 31, 31);
  }
</style>
