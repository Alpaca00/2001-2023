<script>
  export let games = [
    { title: "Halo: Combat Evolved", year: 2001, description: "A groundbreaking first-person shooter." },
    { title: "Grand Theft Auto III", year: 2001, description: "The game that changed open-world gaming forever." },
    { title: "The Sims", year: 2000, description: "A life simulation that became a cultural phenomenon." },
    { title: "Warcraft III: Reign of Chaos", year: 2002, description: "A real-time strategy classic with an epic storyline." },
    { title: "Max Payne", year: 2001, description: "Known for its dark, gritty noir story and groundbreaking bullet-time mechanic." },
    { title: "Star Wars: Knights of the Old Republic", year: 2003, description: "An RPG that became one of the best Star Wars games ever made." },
    { title: "Age of Mythology", year: 2002, description: "A mythological RTS with epic battles and gods." }
  ];
</script>

<div class="container">
  <div class="game-list">
    <h2>🎮 Computer games</h2>
    <ul>
      {#each games as game}
        <li>
          <strong>{game.title}</strong> ({game.year}) - {game.description}
        </li>
      {/each}
    </ul>
  </div>

  <img class="game-poster"
       src="https://upload.wikimedia.org/wikipedia/en/thumb/4/4c/Maxpaynebox.jpg/220px-Maxpaynebox.jpg"
       alt="Max Payne Game Poster">
</div>

<style>
  .container {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    gap: 20px;
    max-width: 900px;
    margin: 20px auto;
  }

  .game-list {
    font-size: 18px;
    color: white;
    text-align: left;
    flex: 1;
    max-width: 500px;
    font-family: "Comic Sans MS", cursive;
  }

  .game-list ul {
    list-style-type: disc;
    padding-left: 20px;
  }

  .game-poster {
    max-width: 250px;
    height: auto;
    border-radius: 10px;
  }
</style>

