<!FOR YOUU BBY>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy New Year ❤️</title>

<style>
body{
  margin:0;
  font-family:'Poppins',sans-serif;
  background:linear-gradient(135deg,#ffd6e8,#fff0f6);
  overflow:hidden;
}

/* flowers falling animation */
.flower{
  position:absolute;
  font-size:22px;
  animation:fall 7s linear infinite;
}
@keyframes fall{
  0%{top:-50px;opacity:1}
  100%{top:110vh;opacity:0}
}

/* page style */
.page{
  width:100%;
  height:100vh;
  display:none;
  justify-content:center;
  align-items:center;
  overflow-y:auto;                  /* scroll allow */
  -webkit-overflow-scrolling: touch; /* smooth scroll mobile */
  padding-bottom:30px;               /* button space */
}
.page.active{display:flex; animation:fadein 0.6s;}
@keyframes fadein{
  from{opacity:0;transform:scale(0.95);}
  to{opacity:1;transform:scale(1);}
}

/* card style */
.card{
  width:90%;
  max-width:360px;
  background:#fff;
  border-radius:25px;
  padding:28px;
  text-align:center;
  box-shadow:0 12px 30px rgba(0,0,0,0.2);
  position:relative;
}

/* envelope flap */
.card::before{
  content:"";
  position:absolute;
  top:-40px;
  left:0;
  width:100%;
  height:80px;
  background:#ff9aa2;
  border-radius:0 0 100% 100%;
}

/* text */
h1{color:#ff4d6d; font-size:28px; margin-top:30px;}
p{font-size:18px; color:#444; line-height:1.6;}
.big{font-size:22px; color:#e63946; font-weight:bold;}

/* button always visible */
button{
  position: sticky;
  bottom:20px;
  margin-top:auto;
  padding:12px 22px;
  border:none;
  border-radius:25px;
  background:#ff4d6d;
  color:white;
  font-size:16px;
  cursor:pointer;
}

/* heart pulse last page */
.heart{
  display:inline-block;
  animation:beat 1s infinite;
}
@keyframes beat{
  0%,100%{transform:scale(1);}
  50%{transform:scale(1.3);}
}
</style>
</head>

<body>

<!-- Background music -->
<audio id="bgMusic" autoplay loop>
  <source src="romantic.mp3" type="audio/mpeg">
</audio>

<!-- flowers -->
<span class="flower" style="left:10%">🌸</span>
<span class="flower" style="left:25%">🌹</span>
<span class="flower" style="left:45%">🌼</span>
<span class="flower" style="left:65%">🌺</span>
<span class="flower" style="left:85%">💐</span>

<!-- PAGE 1 -->
<div class="page active">
  <div class="card">
    <h1>💌 Ek Special Card</h1>
    <p>Sirf meri Billi ke liye ❤️</p>
    <button onclick="nextPage()">Envelope Open Kare ✨</button>
  </div>
</div>

<!-- PAGE 2 -->
<div class="page">
  <div class="card">
    <h1>Happy New Year mera jaan i wish apka yeh saal bakki sbhi salo se bhut acha jaye bby 🎉</h1>
    <p class="big">Meri Billi 🐱 ho na</p>
    <p>
      Aap meri zindagi ka<br>
      sabse pyaara hissa ho aur aage bhi life time tak rahoge ❤️
    </p>
    <button onclick="nextPage()">Aage ➡️</button>
  </div>
</div>

<!-- PAGE 3 -->
<div class="page">
  <div class="card">
    <h1>Special Nicknames 🤍</h1>
    <p>
      Kabhi <b>Bandar</b> 🐒,<br>
      kabhi <b>Chirkut</b> 😄,<br>
      aur hamesha mera  <b>Chhota Bheem</b> 💪❤️
    </p>
    <button onclick="nextPage()">Next 💕</button>
  </div>
</div>

<!-- PAGE 4 -->
<div class="page">
  <div class="card">
    <h1>Ek Vaada 🤞</h1>
    <p class="big">
      Har saal,<br>
      har mood,<br>
      har haal me<br>
      sirf aapka hi rahuga or aap to mera ho hi i know i know mera pyra bacha io na dar ke rah kro mesa badmasi nahi kro kro acha bacha ki tra rho smjheeeeee💖
    </p>
    <button onclick="nextPage()">Last 💝</button>
  </div>
</div>

<!-- PAGE 5 -->
<div class="page">
  <div class="card">
    <h1>Forever ♾️</h1>
    <p class="big heart">I I Love You mera bacha 🐣 ❤️</p>
    <p>
      2025 bhi,<br>
      aur aane wale saare saal apke bhut ache jaye kr mere sath jaye <br>
      aapko hamesha khush rho aur i wish meri bhi saru  khushiyan apko mile hamesa khush rho bacha smile a smile on your face or harmesa filhal ab jyada kuchh To bolane Ko nahin abhi ke liye chalta hun bye bye byee 👋🏻 😊 ✨
    </p>
  </div>
</div>

<script>
let current=0;
const pages=document.querySelectorAll('.page');

function nextPage(){
  pages[current].classList.remove('active');
  current++;
  if(current<pages.length){
    pages[current].classList.add('active');
  }
}

// background music volume
const music=document.getElementById("bgMusic");
music.volume=0.2;
</script>

</body>
</html>
