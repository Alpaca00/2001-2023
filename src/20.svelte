<style>
    body {
        height: 100%;
        background-size: cover;
        overflow: hidden;
        display: flex;
        flex-flow: column wrap;
        justify-content: center;
        align-items: center;
    }

    .text {
        position: relative;
        text-align: center;
        z-index: 1;
    }

    .text h1 {
        color: black;
        font-size: 15em;
        text-align: center;
        text-shadow: -5px 5px 0px rgba(0,0,0,0.7), -10px 10px 0px rgba(0,0,0,0.4), -15px 15px 0px rgba(0,0,0,0.2);
        font-family: monospace;
        font-weight: bold;
    }

    .text h2 {
        color: black;
        font-size: 5em;
        text-shadow: -5px 5px 0px rgba(0,0,0,0.7);
        font-family: monospace;
        font-weight: bold;
    }

    .text h3 {
        color: transparent;
        font-size: 2em;
        text-shadow: -5px 5px 0px rgba(0,0,0,0.7);
        font-family: monospace;
        font-weight: bold;
    }

    .torch {
        position: absolute;
        margin: 0;
        width: 200px;
        height: 200px;
        box-shadow: 0 0 0 9999em #000000f7;
        opacity: 1;
        border-radius: 50%;
        background: rgba(0,0,0,0.3);
        pointer-events: none;
    }

    .torch:after {
        content: '';
        display: block;
        border-radius: 50%;
        width: 100%;
        height: 100%;
        top: 0px;
        left: 0px;
        box-shadow: inset 0 0 40px 2px #000,
        0 0 20px 4px rgba(13,13,10,0.2);
    }
</style>

<div class="text">
    <h1>404</h1>
    <h2>Uh, Ohh</h2>
    <h3>Sorry, we can't find what you are looking for 'cuz it's so dark in here</h3>
</div>

<div class="torch"></div>

<script>
    import { onMount } from 'svelte';

    onMount(() => {
        const torch = document.querySelector('.torch');

        window.addEventListener('mousemove', (e) => {
            const mouseX = e.pageX;
            const mouseY = e.pageY;

            torch.style.left = `${mouseX - torch.offsetWidth / 2}px`;
            torch.style.top = `${mouseY - torch.offsetHeight / 2}px`;
        });
    });
</script>
