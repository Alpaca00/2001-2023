<script>
  export let books = [
    { title: "The Kite Runner", author: "Khaled Hosseini", year: 2003 },
    { title: "The Da Vinci Code", author: "Dan Brown", year: 2003 },
    { title: "Harry Potter and the Order of the Phoenix", author: "J.K. Rowling", year: 2003 },
    { title: "Life of Pi", author: "Yann Martel", year: 2001 },
    { title: "Shantaram", author: "Gregory David Roberts", year: 2003 }
  ];
</script>

<div class="container">
  <div class="book-list">
    <h2>📚 Interesting books</h2>
    <ul>
      {#each books as book}
        <li><strong>{book.title}</strong> by {book.author} ({book.year})</li>
      {/each}
    </ul>
  </div>

  <img class="book-poster"
       src="https://images.renaud-bray.com/images/PG/2131/2131062-gf.jpg?404=404RB.gif"
       alt="Shantaram Book Cover">
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

  .book-list {
    font-size: 18px;
    color: white;
    text-align: left;
    flex: 1;
    max-width: 500px;
    font-family: "Comic Sans MS", cursive;
  }

  .book-list ul {
    list-style-type: square;
    padding-left: 20px;
  }

  .book-poster {
    max-width: 200px;
    height: auto;
    border-radius: 10px;
  }
</style>
