<script>
    import { onMount } from "svelte";
    let message = "The future starts now!";
    let showModal = false;

      function clickMe() {
        showModal = true;
      }

      function confirmRedirect() {
        showModal = false;
        setTimeout(() => {
          window.location.href = "https://eloquence.uno";
        }, 1000);
      }

      function cancelRedirect() {
        showModal = false;
      }


    function showAdError() {
      alert("❌ Error 0x0001: Unknown issue occurred!\n\nPlease contact support via ICQ.");
    }

    onMount(() => {
      console.log("Retro page loaded!");
    });
</script>
<style>
    body {
      font-family: "Comic Sans MS", cursive;
      text-align: center;
      cursor: url("https://cur.cursors-4u.net/cursors/cur-2/cur104.cur"), auto;
      margin: 0;
      padding: 0;
      height: 100%;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 20px;
    }
  .modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    justify-content: center;
    align-items: center;
  }

  .modal.show {
    display: flex;
  }

  .modal-content {
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
    font-family: "Comic Sans MS", cursive;
  }

  .modal-buttons {
    margin-top: 20px;
  }

  .modal-button {
    background: linear-gradient(to bottom, #ffcc00, #ff6600);
    border: 3px solid #ff0000;
    padding: 10px 20px;
    font-size: 18px;
    font-weight: bold;
    color: white;
    text-shadow: 2px 2px 2px black;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
    cursor: pointer;
    transition: background 0.3s ease;
    margin: 0 10px;
  }

  .modal-button:hover {
    background: linear-gradient(to bottom, #ff6600, #ffcc00);
  }
    .retro-button {
    background: linear-gradient(to bottom, #ffcc00, #ff6600);
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

  .retro-loading {
    font-size: 18px;
    color: #ff0000;
    font-family: 'Comic Sans MS', cursive;
    font-weight: bold;
    text-align: center;
    display: none;
    margin-top: 20px;
    text-shadow: 2px 2px 5px yellow;
  }

  .retro-alert {
    color: #ff0000;
    font-size: 16px;
    font-family: 'Comic Sans MS', cursive;
    text-align: center;
    font-weight: bold;
    text-shadow: 2px 2px black;
    display: none;
    margin-top: 20px;
  }

    h1 {
      text-shadow: 3px 3px 5px #ff00ff;
      animation: blink 1s infinite alternate;
    }

    @keyframes blink {
      from { opacity: 1; }
      to { opacity: 0.5; }
    }

    .header, .footer {
      background: linear-gradient(to right, #ff0000, #ff9900);
      color: yellow;
      padding: 15px;
      font-size: 24px;
      font-weight: bold;
      text-shadow: 2px 2px black;
      border: 4px solid black;
    }

    .button {
      background: linear-gradient(to bottom, #ffcc00, #ff6600);
      border: 3px solid #ff0000;
      padding: 15px 30px;
      font-size: 20px;
      font-weight: bold;
      color: white;
      text-shadow: 2px 2px 2px black;
      box-shadow: 5px 5px 10px rgba(0,0,0,0.5);
      cursor: pointer;
    }

    .button:hover {
      background: linear-gradient(to bottom, #ff6600, #ffcc00);
    }

    marquee {
      font-size: 24px;
      color: #00ff00;
      cursor: pointer;
      font-weight: bold;
      background: black;
      padding: 10px;
      border: 3px solid red;
    }

    .content {
      font-size: 24px;
      color: yellow;
    }

    .nostalgia {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 20px;
      margin-top: 20px;
    }

    .nostalgia img {
      width: 150px;
      height: auto;
      border: 5px solid #ff00ff;
      border-radius: 10px;
    }

    .ad-banner {
      background: yellow;
      color: red;
      padding: 10px;
      font-size: 20px;
      font-weight: bold;
      border: 3px solid black;
      margin-top: 20px;
      animation: blink-text 1s infinite alternate;
    }

    @keyframes blink-text {
      0% {
        color: red;
      }
      50% {
        color: transparent;
      }
      100% {
        color: red;
      }
    }

    .book-list {
      margin-top: 20px;
      font-size: 18px;
      color: white;
    }

    .book-list ul {
      list-style-type: square;
      padding-left: 20px;
    }

    .movie-poster {
      margin-top: 20px;
      font-size: 18px;
      color: white;
    }

    .movie-list {
      margin-top: 20px;
      font-size: 18px;
      color: white;
      text-align: left;
      max-width: 500px;
      margin-left: auto;
      margin-right: auto;
    }

    .movie-list ul {
      list-style-type: disc;
      padding-left: 20px;
    }

    .game-list {
      margin-top: 20px;
      font-size: 18px;
      color: white;
      text-align: left;
      max-width: 500px;
      margin-left: auto;
      margin-right: auto;
    }

    .game-list ul {
      list-style-type: disc;
      padding-left: 20px;
    }
    .year-link {
      text-decoration: none;
      color: #007bff;
      font-weight: bold;
      transition: color 0.3s ease;
    }

    .year-link:hover {
      color: #0056b3;
    }
</style>
<div class="top-header" style="display: flex; justify-content: center; gap: 15px; padding: 10px; background-color: black; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); font-size: 18px;">
    <a href="#" class="year-link">2001-2003</a>
    <a class="year-link disabled">2004-2007</a>
    <a class="year-link disabled">2008-2011</a>
    <a class="year-link disabled">2012-2015</a>
    <a class="year-link disabled">2016-2019</a>
    <a class="year-link disabled">2020-2023</a>
</div>
<div class="container">
    <div class="header">
        💾 WELCOME, NET TRAVELER! ENJOY YOUR STAY IN CYBERSPACE! 💾
    </div>
    <div class="support-info" style="position: absolute; font-size: 20px; color=yellow;">
            💬 ICQ: 7123456
    </div><br><br>
    <img src="https://media1.tenor.com/m/mJNke65tYHkAAAAC/oh-boy.gif" alt="Dancing Baby">
    <h1>{message}</h1>
    <marquee behavior="scroll" direction="left" on:click={showAdError}>🔥 CLICK HERE! FREE EMOJIS!!! 1,000,000th VISITOR WINS
        A PRIZE! 🔥
    </marquee>
    <br><br>
    <button class="button" on:click={clickMe}>Hey! Ready to learn foreign languages? Click here!</button>
      <div class="modal {showModal ? 'show' : ''}">
    <div class="modal-content">
      <h2>Are you sure you want to leave this page?</h2>
      <p>You are about to be redirected to an external site.</p>
      <div class="modal-buttons">
        <button class="modal-button" on:click={confirmRedirect}>Yes, take me there!</button>
        <button class="modal-button" on:click={cancelRedirect}>No, stay here</button>
      </div>
    </div>
  </div>

    <div class="movie-list">
        <h2>🎬 Must-See Movies</h2>
        <ul>
            <li><strong>Lord of the Rings: The Fellowship of the Ring</strong> (2001)</li>
            <li><strong>Harry Potter and the Sorcerer's Stone</strong> (2001)</li>
            <li><strong>Spider-Man</strong> (2002)</li>
            <li><strong>The Matrix Reloaded</strong> (2003)</li>
            <li><strong>Finding Nemo</strong> (2003)</li>
            <li><strong>Gladiator</strong> (2000)</li>
            <li><strong>Jurassic Park III</strong> (2001)</li>
        </ul>
    </div>

    <img class="movie-poster" src="https://www.reeldeals.com/images/items/mylarjurassicpark3mini01.jpg"
        alt="Jurassic Park Movie Poster">

    <div class="book-list">
        <h2>📚 Interesting Books</h2>
        <ul>
            <li><strong>The Kite Runner</strong> by Khaled Hosseini (2003)</li>
            <li><strong>The Da Vinci Code</strong> by Dan Brown (2003)</li>
            <li><strong>Harry Potter and the Order of the Phoenix</strong> by J.K. Rowling (2003)</li>
            <li><strong>Life of Pi</strong> by Yann Martel (2001)</li>
            <li><strong>Shantaram</strong> by Gregory David Roberts (2003)</li>
        </ul>
    </div>

    <div class="game-list">
    <h2>🎮 Computer Games</h2>
    <ul>
        <li><strong>Halo: Combat Evolved</strong> (2001) - A groundbreaking first-person shooter.</li>
        <li><strong>Grand Theft Auto III</strong> (2001) - The game that changed open-world gaming forever.</li>
        <li><strong>The Sims</strong> (2000) - A life simulation that became a cultural phenomenon.</li>
        <li><strong>Warcraft III: Reign of Chaos</strong> (2002) - A real-time strategy classic with an epic storyline.</li>
        <li><strong>Max Payne</strong> (2001) - Known for its dark, gritty noir story and groundbreaking bullet-time mechanic.</li>
        <li><strong>Star Wars: Knights of the Old Republic</strong> (2003) - An RPG that became one of the best Star Wars games ever made.</li>
        <li><strong>Age of Mythology</strong> (2002) - A mythological RTS with epic battles and gods.</li>
    </ul>
</div>

    <div class="content">
    <p><strong>Ready to dive into the future?</strong></p>
        <ul>
            <li>Dial-up internet and that weird connection sound 📞</li>
            <li>MSN Messenger and funny screen names 💬</li>
            <li>Neopets, Habbo Hotel, and Club Penguin 🐧</li>
            <li>Watching cartoons on VHS 📼</li>
            <li>Playing Snake on a Nokia 3310 📱</li>
        </ul>
    </div>

    <div class="nostalgia">
        <img src="https://cdn9.neopets.com/headless-cms/US_ARTICLES_NEWS_New_Era_1e9a97b766.png" alt="Neopets Logo">
        <img src="https://seeklogo.com/images/M/msn-messenger-logo-1A0536E047-seeklogo.com.png" alt="MSN Messenger">
        <img src="https://platform.theverge.com/wp-content/uploads/sites/2/chorus/assets/3150371/3310.jpg?quality=90&strip=all&crop=0,0,100,100"
             alt="Nokia 3310">
    </div>

    <div class="ad-banner">💥 WIN A FREE IPOD! CLICK HERE NOW! 💥</div>

    <div class="footer">© 2001-2025
        <blink>little-game.uno</blink>
        | Best viewed in Internet Explorer 6 🚀
    </div>
</div>
