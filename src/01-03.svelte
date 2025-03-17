<script>
    import { onMount } from "svelte";
    import TopHeader from "./components/TopHeader.svelte";
    import Modal from "./components/01-03/Modal.svelte";
    import RetroButton from "./components/01-03/RetroButton.svelte";
    import MarqueeAd from "./components/01-03/MarqueeAd.svelte";
    import MovieList from './components/01-03/content/MovieList.svelte';
    import BookList from './components/01-03/content/BookList.svelte';
    import GameList from './components/01-03/content/GameList.svelte';
    import NostalgiaList from './components/01-03/content/NostalgiaList.svelte';


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

<TopHeader />
<div class="container">
    <div class="header">
        💾 WELCOME, NET TRAVELER! ENJOY YOUR STAY IN CYBERSPACE! 💾
    </div>
    <div class="support-info" style="position: absolute; font-size: 20px; color: yellow;">
            💬 ICQ: 7123456
    </div><br><br>
<div class="left-content">
  <img src="https://media1.tenor.com/m/mJNke65tYHkAAAAC/oh-boy.gif" alt="Dancing Baby">
</div>
<div class="right-content">
  <div class="ad-text">
    <p><strong>Get the latest music, movies, and games here!</strong></p>
    <p>Join the ultimate gaming experience of the millennium. Don't miss out!</p>
  </div>
  <img src="https://supernaturalhippie.com/wp-content/uploads/2019/01/dracula-2000-gif.gif" alt="Funny Gif" class="funny-gif" />
</div>

      <h1>{message}</h1>
      <MarqueeAd {showAdError} />
    <br><br>
  <RetroButton text="Hey! Ready to learn foreign languages? Click here!" onClick={clickMe} />
  <Modal {showModal} {confirmRedirect} {cancelRedirect} />

    <MovieList />
    <BookList />
    <GameList />


    <NostalgiaList />

    <div class="ad-banner">💥 WIN A FREE IPOD! CLICK HERE NOW! 💥</div>

    <div class="footer">© 2001-2025
        <blink>little-game.uno</blink>
        | Best viewed in Internet Explorer 6 🚀
    </div>
</div>

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
      font-family: "Comic Sans MS", cursive;
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
      font-family: "Times New Roman", serif;
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

  .left-content,
  .right-content {
    display: inline-block;
    vertical-align: top;
    width: 48%;
    padding: 10px;
  }

  .left-content img,
  .right-content .funny-gif {
    width: 50%;
    height: 50%;
  }

  .right-content {
    text-align: center;
    color: yellow;
    font-family: "Comic Sans MS", cursive;
  }

  .right-content .ad-text {
    font-size: 18px;
    margin-bottom: 10px;
  }
</style>