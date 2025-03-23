<body>
<h2>Gotcha! Now you're trapped;)</h2>
<h3>Code 403</h3>
<div id="jail">
    <svg xmlns="http://www.w3.org/2000/svg"
         xmlns:xlink="http://www.w3.org/1999/xlink"
         version="1.1"
         viewBox="0 0 1000 1000"
         preserveAspectRatio="xMinYMin"
         id="spinner">
        <defs>
            <path id="textPath" d="M 250 500 A 250,250 0 1 1 250 500.0001" />
        </defs>
    </svg>
    <div id="cursor"></div>
</div>
</body>

<script>
  document.addEventListener("mousemove", (e) => {
    document.body.classList.add("seenMouse");

    const cursor = document.getElementById("cursor");
    const jail = document.getElementById("jail");

    const jailRect = jail.getBoundingClientRect();

    const radius = jailRect.width / 2;
    const centerX = jailRect.left + radius;
    const centerY = jailRect.top + radius;

    let deltaX = e.clientX - centerX;
    let deltaY = e.clientY - centerY;

    const distance = Math.sqrt(deltaX * deltaX + deltaY * deltaY);

    if (distance > radius) {
      const angle = Math.atan2(deltaY, deltaX);
      deltaX = Math.cos(angle) * radius;
      deltaY = Math.sin(angle) * radius;
    }

    cursor.style.transform = `translate(${deltaX + radius}px, ${deltaY + radius}px)`;
  });
</script>

<style>
    body {
        height: 100vh;
        display: flex;
        flex-direction: column;
        background-color: #111;
        align-items: center;
        justify-content: center;
        cursor: none;
        overflow: hidden;
        color: white;
    }

    h2 {
        font-size: 5vmin;
        margin-bottom: 0;
        text-shadow: 0 0 10px #ff0000;
    }

    h3 {
        font-size: 4vmin;
        margin-top: 0;
        margin-bottom: 40px;
        text-shadow: 0 0 5px rgba(255, 255, 255, 0.5);
    }

    #jail {
        position: relative;
        border: 2px solid gray;
        border-radius: 50%;
        width: 300px;
        height: 300px;
    }

    #spinner {
        display: none;
        position: absolute;
        width: 120px;
        height: 120px;
        left: 50%;
        top: 50%;
        transform-origin: 50% 50%;
        animation: 4s spin linear infinite;
        fill: white;
    }

    body.seenMouse #spinner {
        display: block;
    }

    #cursor {
        position: absolute;
        width: 32px;
        height: 32px;
        background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAABmJLR0QAAAAAAAD5Q7t/AAABX0lEQVRYw+3UMUvDUBQF4EOv3Nk2OnjxB4gg6OQo2Nm/5c9w0snJyUWlKAhBEaRgKypiiK/FrdBCad/NdWkgFnHyNUvOEshyPk5eHoilRyy7KCm12fOwNASx9D5d34jlshQEsfTMzEpD5IDSEEVAKYh5wMIRvwFU1ZIkXQxiHqCqNp1ObTwe2+vbe3hEEVAsH41GNhgM7OmpGxSRX0TIsgxZlkFVoarw3kNVsbLSwH18vo9Al1Xtr3LvPbz3iKI6bm/O9gEc/jdgKQfk5WnqsLoawXuPtfXtqxCz/wix9PJv/vz8YsQyPD45NeecEcsFsRwEBxTLiWWXWNpJklgc3xmxtEP21wAgTR02t/ZGAJo6cTGAj4eHNhqNZQD4CLrC7BcbFk/4bIVOt9u1VuvaiOUxVP+STlxz/qVOXEwsb/3+10YU1QFgGmyBP5YRYukQyxGx7CwcUKVKlSpVqiwq37opL7UKP+WdAAAAAElFTkSuQmCC);
    }

    @keyframes spin {
        0% {
            transform: translate(-50%, -50%) rotate(360deg);
        }
        100% {
            transform: translate(-50%, -50%) rotate(0deg);
        }
    }
</style>
