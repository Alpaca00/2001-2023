<script>
  export let src;
</script>

<div class="iframe-container">
  <iframe
    src={src}
    width="100%"
    height="100%"
    style="border: none;"
    allowfullscreen
  ></iframe>
</div>

<style>
  .iframe-container {
  position: relative;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  iframe {
    width: 100%;
    height: 100%;
  }
</style>
