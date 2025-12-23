<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Happy Birthday Bitu Mama ❤️</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Poppins:wght@300;400;600&family=Pacifico&display=swap');

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  /* More colorful, vibrant gradient */
  background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
  background-size: 400% 400%;
  animation: gradientBG 15s ease infinite;
  height:100vh;
  overflow:hidden;
  font-family: 'Poppins', sans-serif;
  color: #333;
}

@keyframes gradientBG {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

/* Star/Sparkle decorations */
.star {
  position: absolute;
  background: white;
  border-radius: 50%;
  opacity: 0.5;
  animation: twinkle var(--duration) infinite;
}

@keyframes twinkle {
  0%, 100% { opacity: 0.3; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.2); }
}

.slide{
  display:none;
  height:100vh;
  width:100%;
  align-items:center;
  justify-content:center;
  flex-direction:column;
  text-align:center;
  padding:30px;
  transition: all 0.8s ease-in-out;
  z-index: 2;
  position: relative;
}

.slide.active{
  display:flex;
  animation: fadeIn 1s forwards;
}

@keyframes fadeIn {
  from { opacity: 0; transform: scale(0.9); }
  to { opacity: 1; transform: scale(1); }
}

.glass-card {
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(15px);
  border: 2px solid rgba(255, 255, 255, 0.5);
  padding: 40px;
  border-radius: 30px;
  box-shadow: 0 15px 35px rgba(0,0,0,0.2);
  max-width: 600px;
}

.icon-img {
  width: 140px;
  height: 140px;
  margin-bottom: 20px;
  filter: drop-shadow(0 10px 15px rgba(0,0,0,0.2));
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(5deg); }
}

button {
  padding: 15px 40px;
  border: none;
  border-radius: 50px;
  background: linear-gradient(45deg, #ff4b5c, #f8b500);
  color: white;
  font-size: 1.1rem;
  font-weight: 600;
  cursor: pointer;
  margin-top: 25px;
  transition: 0.3s;
  box-shadow: 0 5px 20px rgba(255, 75, 92, 0.5);
}

button:hover { transform: scale(1.1) rotate(-2deg); }

.countdown { display: flex; gap: 15px; margin: 20px 0; }
.box { 
    background: white; 
    padding: 20px; 
    border-radius: 15px; 
    min-width: 90px; 
    font-weight: bold; 
    border-bottom: 5px solid #ff4b5c;
}

#note {
  max-width: 550px;
  font-size: 22px;
  background: #fffdf5;
  padding: 40px;
  border-radius: 15px;
  box-shadow: 10px 10px 30px rgba(0,0,0,0.15);
  text-align: left;
  line-height: 1.8;
  font-family: 'Dancing Script', cursive;
  white-space: pre-wrap; 
  border-left: 10px solid #ff4b5c;
  position: relative;
}

.photo {
  width: 250px;
  height: 250px;
  border-radius: 50%;
  border: 8px solid white;
  object-fit: cover;
  box-shadow: 0 15px 40px rgba(0,0,0,0.4);
  margin-bottom: 20px;
}

.confetti { position: absolute; top: -10px; width: 15px; height: 15px; border-radius: 3px; animation: fall 4s linear forwards; z-index: 1;}
@keyframes fall { to { transform: translateY(110vh) rotate(720deg); } }

.balloon { position: absolute; bottom: -100px; font-size: 60px; animation: fly 10s linear infinite; z-index: 1; filter: opacity(0.8);}
@keyframes fly { to { transform: translateY(-120vh) translateX(100px); } }
</style>
</head>

<body>

<audio id="music" loop>
  <source src="birthday.mp3" type="audio/mpeg">
</audio>

<div id="star-container"></div>

<div class="slide active">
  <img src="https://cdn-icons-png.flaticon.com/512/833/833472.png" class="icon-img">
  <div class="glass-card">
    <h1 style="font-family: 'Pacifico', cursive; font-size: 3rem; color: #ff4b5c;">Something special...</h1>
    <p style="font-size: 1.2rem;">Is arriving for Bitu Mama.</p>
  </div>
</div>

<div class="slide">
  <img src="https://cdn-icons-png.flaticon.com/512/2488/2488614.png" class="icon-img">
  <h2 style="color: white; text-shadow: 2px 2px 10px rgba(0,0,0,0.2);">The Wait is Almost Over</h2>
  <div class="countdown">
    <div class="box">00<br><small>DAYS</small></div>
    <div class="box">00<br><small>HRS</small></div>
    <div class="box">00<br><small>MINS</small></div>
    <div class="box" id="secs" style="color: #ff4b5c;">05<br><small>SEC</small></div>
  </div>
</div>

<div class="slide">
  <img src="https://cdn-icons-png.flaticon.com/512/4213/4213958.png" class="icon-img">
  <div class="glass-card">
    <h2>Ready to celebrate?</h2>
    <button onclick="startMagic()">TAP TO UNWRAP 🎁</button>
  </div>
</div>

<div class="slide">
  <img src="https://cdn-icons-png.flaticon.com/512/3132/3132693.png" class="icon-img">
  <h1 style="font-size: 4rem; color: white; text-shadow: 3px 3px 0px #d63031; font-family: 'Pacifico', cursive;">Happy Birthday, <br>Bitu Mama!</h1>
  <button onclick="nextSlide()">See your message</button>
</div>

<div class="slide">
  <div class="glass-card">
    <h3 style="font-family: 'Pacifico', cursive; color: #ff4b5c; font-size: 2rem;">A Special Note</h3>
    <img src="https://cdn-icons-png.flaticon.com/512/2663/2663067.png" 
         style="width:120px; cursor:pointer; margin-top:20px;" 
         onclick="showNote()">
    <p style="margin-top:10px;"><b>Tap the letter to open</b></p>
  </div>
</div>

<div class="slide">
  <div id="note"></div>
  <button onclick="nextSlide()">Final Surprise</button>
</div>

<div class="slide">
  <img src="Screenshot_2025-12-21-21-38-27-079_com.instagram.android.jpg" class="photo" alt="Bitu Mama">
  <div class="glass-card">
    <p style="font-size:22px; font-weight: 500; color: #333;">
      Wishing you a joyful birthday filled with peace, good health, and the love of those who hold you dear.
    </p>
    <h1 style="margin-top:20px; color: #ff4b5c; font-family: 'Pacifico', cursive; font-size: 2.5rem;">Happy Birthday Mama</h1>
  </div>
</div>

<script>
let current = 0;
const slides = document.querySelectorAll('.slide');
const music = document.getElementById('music');

// Generate background stars
function createStars() {
  const container = document.getElementById('star-container');
  for (let i = 0; i < 50; i++) {
    const star = document.createElement('div');
    star.className = 'star';
    const size = Math.random() * 4 + 'px';
    star.style.width = size;
    star.style.height = size;
    star.style.top = Math.random() * 100 + 'vh';
    star.style.left = Math.random() * 100 + 'vw';
    star.style.setProperty('--duration', (Math.random() * 3 + 2) + 's');
    container.appendChild(star);
  }
}
createStars();

function nextSlide(){
  slides[current].classList.remove('active');
  current++;
  if(current < slides.length) slides[current].classList.add('active');
  if(current === 3 || current === 6) startBalloons();
}

setTimeout(nextSlide, 3500);

let sec = 5;
const countdownInterval = setInterval(() => {
  sec--;
  const secBox = document.getElementById('secs');
  if(secBox) secBox.innerHTML = `0${sec}<br><small>SEC</small>`;
  if(sec <= 0) {
    clearInterval(countdownInterval);
    nextSlide();
  }
}, 1000);

function startMagic(){
  music.volume = 0.5;
  music.play().catch(e => console.log("Audio needs interaction"));
  confettiEffect();
  nextSlide();
}

function confettiEffect(){
  const colors = ['#ff4b5c', '#f8b500', '#23a6d5', '#23d5ab', '#ffffff'];
  for(let i=0; i<80; i++){
    let c = document.createElement('div');
    c.className = 'confetti';
    c.style.left = Math.random() * 100 + 'vw';
    c.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
    c.style.width = Math.random() * 15 + 5 + 'px';
    c.style.height = c.style.width;
    document.body.appendChild(c);
    setTimeout(() => c.remove(), 4000);
  }
}

function startBalloons(){
  setInterval(() => {
    let b = document.createElement('div');
    b.className = 'balloon';
    b.innerText = ['🎈', '✨', '🎊', '💖', '🎂'][Math.floor(Math.random()*5)];
    b.style.left = Math.random() * 100 + 'vw';
    document.body.appendChild(b);
    setTimeout(() => b.remove(), 8000);
  }, 1000);
}

function showNote(){
  nextSlide();
  const text = "Dear  Mama  ❤️,\n\nYou  are  the  heart  of  our  family,  the  calm  in  our  storms,  and  the  reason  our  smiles  feel  complete.\n\nYour  love,  care,  and  strength  inspire  us  every  single  day.\n\nMay  this  year  bring  you  as  much  happiness  as  you  give  to  everyone  around  you.\n\nHappy  Birthday,  Mama!  💖";
  
  let i = 0;
  const noteElement = document.getElementById('note');
  noteElement.innerText = "";
  
  const typing = setInterval(() => {
    noteElement.innerText += text[i];
    i++;
    if(i >= text.length) clearInterval(typing);
  }, 45);
}
</script>

</body>
</html>
