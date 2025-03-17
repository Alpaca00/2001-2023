<script>
  export let showModal;
  export let confirmRedirect;
  export let cancelRedirect;
</script>

<div class="modal {showModal ? 'show' : ''}">
  <div class="modal-content">
    <h2>Are you sure you want to leave this page?</h2>
    <p>You are about to be redirected to an external site.</p>
    <div class="modal-buttons">
      <button class="modal-button" on:click={confirmRedirect}>Yes</button>
      <button class="modal-button" on:click={cancelRedirect}>No</button>
    </div>
  </div>
</div>

<style>
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
    background-color: floralwhite;
    padding: 20px;
    border-radius: 2px;
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
    font-family: "Comic Sans MS", cursive;
  }

  .modal-button:hover {
    background: linear-gradient(to bottom, #ff6600, #ffcc00);
  }
</style>
