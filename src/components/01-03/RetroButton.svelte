<script>
  export let text;
  export let onClick;
</script>

<button class="retro-button" on:click={onClick}>{text}</button>

<style>
  .retro-button {
    background: linear-gradient(to bottom, #ffcc00, #ff6600);
    font-family: "Times New Roman", serif;
    border: 3px solid #ff0000;
    padding: 15px 30px;
    font-size: 20px;
    font-weight: bold;
    color: white;
    text-shadow: 2px 2px 2px black;
    box-shadow: 5px 5px 10px rgba(0,0,0,0.5);
    cursor: pointer;
    transition: background 0.3s ease;
  }

  .retro-button:hover {
    background: linear-gradient(to bottom, #ff6600, #ffcc00);
  }
</style>
