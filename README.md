<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Crystyle 💖</title>

<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.9.3/dist/confetti.browser.min.js"></script>

<style>
body {
margin: 0;
min-height: 100vh;
display: flex;
justify-content: center;
align-items: center;
background: linear-gradient(135deg, #ffe0ec, #fff5f9);
font-family: "Segoe UI", system-ui, sans-serif;
}

.card {
background: white;
border-radius: 24px;
padding: 32px 24px;
width: min(420px, 90%);
text-align: center;
box-shadow: 0 20px 50px rgba(0,0,0,.15);
}

.card img {
width: 220px;
max-width: 80%;
margin-bottom: 18px;
}

h1 {
font-size: 28px;
margin-bottom: 24px;
}

.buttons {
display: flex;
justify-content: center;
gap: 20px;
margin-top: 10px;
}

button {
padding: 14px 26px;
font-size: 18px;
font-weight: 700;
border-radius: 999px;
border: none;
cursor: pointer;
box-shadow: 0 8px 18px rgba(0,0,0,.15);
transition: transform .15s ease;
}

#yes {
background: #ff4d7d;
color: white;
}

#no {
background: #e5e7eb;
}

button:hover {
transform: scale(1.08);
}

.result {
display: none;
margin-top: 22px;
font-size: 26px;
}
</style>
</head>

<body>

<div class="card">

<img
src="https://i.imgur.com/7kJp9wP.png"
alt="Cute Valentine Illustration"
/>

<h1>Crystyle, will you be my Valentine? 💖</h1>

<div class="buttons">
<button id="yes">Yes 💕</button>
<button id="no">No 😅</button>
</div>

<div class="result" id="result">
You just made my heart smile 💘
</div>

</div>

<script>
const yes = document.getElementById("yes");
const no = document.getElementById("no");
const result = document.getElementById("result");

no.addEventListener("mouseover", () => {
no.style.position = "absolute";
no.style.left = Math.random() * 70 + "%";
no.style.top = Math.random() * 70 + "%";
});

yes.addEventListener("click", () => {
result.style.display = "block";
confetti({
particleCount: 200,
spread: 120,
origin: { y: 0.6 }
});
});
</script>

</body>
</html>
