<script>
  export let movies = [
    { title: "Lord of the Rings: The Fellowship of the Ring", year: 2001 },
    { title: "Harry Potter and the Sorcerer's Stone", year: 2001 },
    { title: "Spider-Man", year: 2002 },
    { title: "The Matrix Reloaded", year: 2003 },
    { title: "Finding Nemo", year: 2003 },
    { title: "Gladiator", year: 2000 },
    { title: "Jurassic Park III", year: 2001 }
  ];
</script>

<div class="movie-list">
  <h2>🎬 Must-see movies</h2>
  <ul>
    {#each movies as movie}
      <li><strong>{movie.title}</strong> ({movie.year})</li>
    {/each}
  </ul>
</div>
<img class="movie-poster" src="https://www.reeldeals.com/images/items/mylarjurassicpark3mini01.jpg"
    alt="Jurassic Park Movie Poster">
<style>
    .movie-list {
      margin-top: 20px;
      font-size: 18px;
      color: white;
      text-align: left;
      max-width: 500px;
      margin-left: auto;
      margin-right: auto;
      font-family: "Comic Sans MS", cursive;
    }

    .movie-list ul {
      list-style-type: disc;
      padding-left: 20px;
    }
    .movie-poster {
      max-width: 50%;
      height: auto;
    }
</style>
