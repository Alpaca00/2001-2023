<script>
  export let items = [
    "Dial-up internet and that weird connection sound 📞",
    "MSN Messenger and funny screen names 💬",
    "Neopets, Habbo Hotel, and Club Penguin 🐧",
    "Watching cartoons on VHS 📼",
    "Playing Snake on a Nokia 3310 📱"
  ];
</script>

<div class="content">
  <p><strong>Ready to dive into the future?</strong></p>
  <ul>
    {#each items as item}
      <li>{item}</li>
    {/each}
  </ul>
</div>

<div class="nostalgia">
    <img src="https://cdn9.neopets.com/headless-cms/US_ARTICLES_NEWS_New_Era_1e9a97b766.png" alt="Neopets Logo">
    <img src="https://seeklogo.com/images/M/msn-messenger-logo-1A0536E047-seeklogo.com.png" alt="MSN Messenger">
    <img src="https://platform.theverge.com/wp-content/uploads/sites/2/chorus/assets/3150371/3310.jpg?quality=90&strip=all&crop=0,0,100,100"
         alt="Nokia 3310">
</div>

<style>
    .content {
      font-size: 24px;
      color: yellow;
      font-family: "Comic Sans MS", cursive;
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
</style>
