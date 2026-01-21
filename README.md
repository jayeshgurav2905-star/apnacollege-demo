<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>I Love You Saniya ❤️</title>
<style>
    body {
        margin: 0;
        height: 100vh;
        background: linear-gradient(135deg, #ff758c, #ff7eb3);
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: 'Segoe UI', sans-serif;
        overflow: hidden;
    }

    .card {
        background: white;
        width: 350px;
        padding: 30px;
        border-radius: 20px;
        text-align: center;
        box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        display: none;
        animation: pop 1s ease;
    }

    @keyframes pop {
        from { transform: scale(0); }
        to { transform: scale(1); }
    }

    .ribbon {
        position: absolute;
        width: 100%;
        height: 100%;
        background: #ff4d6d;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        font-size: 24px;
        cursor: pointer;
        animation: pulse 1.5s infinite;
    }

    @keyframes pulse {
        0% { transform: scale(1); }
        50% { transform: scale(1.05); }
        100% { transform: scale(1); }
    }

    h1 {
        color: #ff4d6d;
    }

    .btn {
        margin: 10px;
        padding: 10px 20px;
        border: none;
        border-radius: 20px;
        font-size: 16px;
        cursor: pointer;
    }

    .yes {
        background: #ff4d6d;
        color: white;
    }

    .no {
        background: #ddd;
    }

    .message {
        margin-top: 15px;
        font-size: 18px;
        color: #444;
    }
</style>
</head>

<body>

<div class="ribbon" onclick="openCard()">
    🎀 Tap to Cut the Ribbon 🎀
</div>

<div class="card" id="card">
    <h1>I Love You Saniya ❤️</h1>
    <p>🌸 You make my world beautiful 🌸</p>

    <p><strong>Do you love me? 💖</strong></p>
    <button class="btn yes" onclick="reply('yes')">Yes 😍</button>
    <button class="btn no" onclick="reply('no')">No 🙈</button>

    <p><strong>Will you marry me? 💍</strong></p>
    <button class="btn yes" onclick="reply('marry')">Yes 💕</button>

    <div class="message" id="message"></div>
</div>

<script>
function openCard() {
    document.querySelector('.ribbon').style.display = 'none';
    document.getElementById('card').style.display = 'block';
}

function reply(type) {
    const msg = document.getElementById('message');
    if(type === 'yes') {
        msg.innerHTML = "😍 I knew it! You made my day ❤️";
    } else if(type === 'no') {
        msg.innerHTML = "😢 It's okay… I still care 💗";
    } else {
        msg.innerHTML = "💍 Yayyy! My heart is full of love ❤️✨";
    }
}
</script>

</body>
</html>
