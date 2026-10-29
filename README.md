# for-my-cassy
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Baby ♡</title>
<style>
* { box-sizing: border-box; }
body {
  margin: 0;
  background: #fff4f7;
  color: #8e435c;
  font-family: Georgia, serif;
  text-align: center;
  overflow-x: hidden;
}
header { padding: 65px 20px 35px; }
.bow { font-size: 42px; }
h1 { font-size: clamp(32px, 8vw, 52px); margin: 15px 0; }
p { line-height: 1.9; }
button {
  background: #e88eaa;
  border: none;
  border-radius: 30px;
  color: white;
  padding: 14px 23px;
  font-size: 15px;
  cursor: pointer;
  margin: 8px;
}
button:hover { background: #d96f91; }
section {
  max-width: 560px;
  margin: 22px auto;
  padding: 30px 23px;
  width: calc(100% - 30px);
  background: #ffffffc9;
  border: 1px solid #f6d3df;
  border-radius: 24px;
  box-shadow: 0 8px 25px #e9a8bd20;
}
h2 { color: #d66f91; }
.letter { text-align: left; white-space: pre-line; }
.heart { position: fixed; top: -30px; animation: fall 7s linear infinite; pointer-events:none; z-index: 3; }
@keyframes fall {
  to { transform: translateY(110vh) rotate(360deg); }
}
#surprise { display: none; font-size: 18px; line-height: 2; }
footer { padding: 30px; font-size: 13px; }
</style>
</head>
<body>
<header>
  <div class="bow">🎀</div>
  <p>♡ a little something just for you ♡</p>
  <h1>For My Baby</h1>
  <p>To the girl who makes my world a little more beautiful.</p>
  <button onclick="document.getElementById('letter').scrollIntoView({behavior:'smooth'})">
    Open your gift 💌
  </button>
</header>
<section id="letter">
  <h2>💌 A letter for you</h2>
  <div class="letter">My babyyy,
I wish I could put into words just how much you mean to me. You make my days better just by being in them, and even the smallest things about you make me smile.
You are someone so special to me, and I hope you never forget how loved and appreciated you are. Even when we're far apart, you're still someone I think about every day.
If I could give you one thing, it would be the ability to see yourself through my eyes. Maybe then you'd understand just how precious you are to me.
Thank you for being you, baby. I hope this little website reminds you that somewhere in this big world, there's someone who is so, so happy to have you.
I love you more than these words can ever explain. ♡
Forever your girl,
Your baby 🎀</div>
</section>
<section>
  <h2>Reasons why I love you ♡</h2>
  <p>🎀 Your smile</p>
  <p>🧸 The way you make me feel loved</p>
  <p>💗 Your little habits that make you YOU</p>
  <p>🌷 How you make ordinary days special</p>
  <p>💌 Simply because you're you.</p>
  <button onclick="showReason()">One more reason? ♡</button>
  <p id="reason"></p>
</section>
<section>
  <h2>A tiny reminder 🌷</h2>
  <p>On your good days, I'll celebrate with you.</p>
  <p>On your bad days, I'll be here for you.</p>
  <p>And on the ordinary days, I'll keep finding little ways to love you.</p>
</section>
<section>
  <h2>One last thing, baby… 💗</h2>
  <p>There's a little surprise waiting for you.</p>
  <button onclick="reveal()">Tap to open your surprise 🎁</button>
  <div id="surprise">
    💗 I CHOOSE YOU. EVERY SINGLE TIME. 💗
    <p>In every lifetime, in every universe, I hope I find my way back to you.</p>
    <p>You're my favourite person, babyyy. I love you! 💋</p>
    <div style="font-size:45px">💐💌💗</div>
  </div>
</section>
<footer>
  made with all my love, just for you ♡<br>
  <span id="date"></span>
</footer>
<script>
document.getElementById("date").textContent =
  "A little gift made with love · " + new Date().getFullYear();
const hearts = ["💗","♡","💕","🎀"];
for (let i = 0; i < 18; i++) {
  const h = document.createElement("div");
  h.className = "heart";
  h.textContent = hearts[Math.floor(Math.random()*hearts.length)];
  h.style.left = Math.random()*100 + "vw";
  h.style.animationDelay = Math.random()*7 + "s";
  h.style.animationDuration = (5+Math.random()*6) + "s";
  h.style.fontSize = (14+Math.random()*15) + "px";
  document.body.appendChild(h);
}
const reasons = [
  "Because you make my heart feel at home. 🏡💗",
  "Because even a little message from you makes me smile. 💌",
  "Because you're my favourite notification. 🎀",
  "Because I get to love someone as special as you. 🌷",
  "Because no one else is YOU. And that's my favourite thing. ♡"
];
let index = 0;
function showReason() {
  document.getElementById("reason").textContent =
    reasons[index++ % reasons.length];
}
function reveal() {
  document.getElementById("surprise").style.display = "block";
  document.getElementById("surprise").scrollIntoView({behavior:"smooth",block:"center"});
}
</script>
</body>
</html>

