<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy New Year Mommy</title>
<style>
    body {
        margin: 0;
        padding: 0;
        height: 100vh;
        background: linear-gradient(135deg, #ffb6c1, #ffd1dc, #fff0f5);
        font-family: 'Comic Sans MS', cursive;
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
    }

    .card {
        background: rgba(255, 255, 255, 0.9);
        padding: 40px;
        border-radius: 25px;
        text-align: center;
        box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        animation: pop 1.5s ease;
        z-index: 2;
    }

    @keyframes pop {
        0% { transform: scale(0.3); opacity: 0; }
        100% { transform: scale(1); opacity: 1; }
    }

    h1 {
        color: #ff4d6d;
        font-size: 3em;
        animation: glow 2s infinite alternate;
    }

    @keyframes glow {
        from { text-shadow: 0 0 5px #ff8fa3; }
        to { text-shadow: 0 0 20px #ff4d6d; }
    }

    p {
        font-size: 1.5em;
        color: #555;
    }

    .emoji {
        font-size: 2.5em;
        animation: bounce 1.5s infinite;
    }

    @keyframes bounce {
        0%, 100% { transform: translateY(0); }
        50% { transform: translateY(-15px); }
    }

    .heart {
        position: absolute;
        bottom: -50px;
        font-size: 2em;
        animation: floatUp 6s linear infinite;
        opacity: 0.8;
    }

    @keyframes floatUp {
        0% {
            transform: translateY(0) rotate(0deg);
            opacity: 1;
        }
        100% {
            transform: translateY(-110vh) rotate(360deg);
            opacity: 0;
        }
    }

    .sticker {
        position: absolute;
        font-size: 3em;
        animation: wiggle 3s infinite;
    }

    @keyframes wiggle {
        0% { transform: rotate(0deg); }
        25% { transform: rotate(5deg); }
        50% { transform: rotate(-5deg); }
        75% { transform: rotate(5deg); }
        100% { transform: rotate(0deg); }
    }
</style>
</head>
<body>

<!-- Stickers -->
<div class="sticker" style="top: 20px; left: 30px;">🎀</div>
<div class="sticker" style="top: 50px; right: 40px;">🌸</div>
<div class="sticker" style="bottom: 40px; left: 50px;">🧸</div>
<div class="sticker" style="bottom: 60px; right: 60px;">✨</div>

<div class="card">
    <h1>🎆 Happy New Year Mommy! 🎆</h1>
    <p>
        I love you so much, Mommy! 💖<br>
        Thank you for your love, care, and kindness 🌷<br>
        Wishing you happiness, good health, and smiles all year long 💕
    </p>
    <div class="emoji">🥰💐🎉</div>
</div>

<script>
    function createHeart() {
        const heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "💖";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.animationDuration = (3 + Math.random() * 3) + "s";
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 6000);
    }

    setInterval(createHeart, 300);
</script>

</body>
</html>
