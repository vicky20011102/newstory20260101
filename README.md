<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<title>Dear 黃小黑</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
@font-face {
  font-family: 'Handwrite';
  src: url('./jf-openhuninn-2.1.ttf') format('truetype');
}

body {
  margin: 0;
  font-family: 'Handwrite', cursive;
  background: linear-gradient(180deg, #fff6eb, #ffffff);
  color: #3a2f2f;
  overflow-y: auto;
  padding-top: 60px;
}

.card, .celebrate {
  width: 92%;
  max-width: 390px;
  margin: 0 auto 60px auto;
  border-radius: 26px;
  padding: 54px 28px 60px;
  box-shadow: 0 20px 40px rgba(0,0,0,0.15);
  text-align: center;
  position: relative;
  background: #ffffff;
}

.anpanman {
  width: 82px;
  position: absolute;
  top: -42px;
  left: 50%;
  transform: translateX(-50%);
  animation: jump 1.2s ease-in-out infinite;
}

@keyframes jump {
  0%,100% { transform: translateX(-50%) translateY(0); }
  50% { transform: translateX(-50%) translateY(-6px); }
}

h2 {
  font-size: 26px;
  margin-bottom: 36px;
  letter-spacing: 2px;
}

.section {
  display: none;
  font-size: 21px;
  line-height: 1.9;
  animation: fadeUp 0.8s ease forwards;
  margin-bottom: 28px;
}

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(12px); }
  to { opacity: 1; transform: translateY(0); }
}

button {
  margin-top: 28px;
  padding: 12px 26px;
  font-size: 18px;
  border-radius: 999px;
  border: none;
  background: #ffd2c2;
  color: #3a2f2f;
  cursor: pointer;
  font-family: 'Handwrite', cursive;
}

.choice {
  display: none;
  margin-top: 36px;
}

.choice button {
  margin: 10px;
  padding: 14px 30px;
  font-size: 20px;
}

.music-btn {
  position: fixed;
  top: 16px;
  left: 16px;
  z-index: 999;
}

.celebrate {
  display: none;
  background: linear-gradient(180deg, #ffe4e1, #fff0f5);
  box-shadow: none;
  text-align: center;
  position: relative;
  padding: 80px 28px 60px;
  min-height: 100vh;
  overflow: hidden;
}

.celebrate p {
  font-size: 22px;
  line-height: 1.9;
  opacity: 0;
  animation: fadeIn 1.5s forwards;
  margin: 16px 0;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

/* 粉色星光粒子 */
.star {
  position: absolute;
  width: 6px;
  height: 6px;
  background: #ffb6c1;
  border-radius: 50%;
  animation: fall linear infinite;
}

/* 心形跳動 */
.heart {
  position: absolute;
  top: 50%;
  left: 50%;
  font-size: 80px;
  transform: translate(-50%, -50%);
  color: #ff6b81;
  animation: heartbeat 1.2s infinite;
  opacity: 0;
}

@keyframes heartbeat {
  0%,100% { transform: translate(-50%, -50%) scale(1); }
  50% { transform: translate(-50%, -50%) scale(1.15); }
}

/* 煙火粒子 */
.firework-particle {
  position: absolute;
  border-radius: 50%;
  pointer-events: none;
  opacity: 1;
}
</style>
</head>
<body>

<!-- 音樂控制 -->
<div class="music-btn">
  <button id="musicBtn">🎵 播放音樂</button>
</div>
<audio id="bgm" loop>
  <source src="M5000045Tg2r0WFyt3.mp3" type="audio/mpeg">
</audio>

<!-- 告白卡片 -->
<div class="card">
  <img src="S__86638699.jpg" class="anpanman" alt="麵包超人">
  <h2>Dear 黃小黑</h2>

  <div class="section">
    有時候，<br>
    緣分真的是一件很奇妙的事情。<br><br>
    剛認識你的時候，<br>
    我從來沒有想過，<br>
    後來的故事會走向現在這樣。
  </div>

  <div class="section">
    很幸運，<br>
    在 2025 年的最後遇見你。<br><br>
    謝謝你讓我知道，<br>
    原來我是可以被寵著、被愛著的。<br>
    謝謝你接受我的任性、我的脾氣，<br>
    也謝謝你，這麼這麼地愛我。
  </div>

  <div class="section">
    之前每一次你偷偷告白，<br>
    我都選擇拒絕你。<br><br>
    直到那一天，<br>
    聽到你要被召回的時候，<br>
    我的腦海裡只剩下一個念頭——<br>
    我希望你可以平安回來。
  </div>

  <div class="section">
    那一刻，<br>
    我才發現，<br>
    我是真的愛上你。<br><br>
    而你，<br>
    也真的走進我的心裡了。
  </div>

  <div class="section">
    也許我對感情還是會害怕、會不安，<br>
    我們之間也還有很多要磨合、要學習的地方。<br><br>
    但因為是你，<br>
    所以我想再勇敢一次。<br>
    我不想再讓你等我了。
  </div>

  <div class="section">
    小朋友，<br>
    我喜歡你。<br>
    你願意當我的女朋友嗎？
  </div>

  <button id="nextBtn">往下閱讀</button>

  <div class="choice">
    <button class="agree">願意</button>
    <button class="agree">願意</button>
  </div>
</div>

<!-- 紀念畫面 -->
<div class="celebrate" id="celebrate">
  <p>
    雖然跨年沒能一起看煙火，<br>
    但心永遠在一起
  </p>
  <p>2026.01.01 新的開始</p>
  <p>黃小黑跟廖小白在一起啦！</p>
  <div class="heart">❤️</div>
</div>

<script>
// 分段閱讀
const sections = document.querySelectorAll('.section');
const nextBtn = document.getElementById('nextBtn');
const choice = document.querySelector('.choice');
let current = 0;
sections[0].style.display = 'block';

nextBtn.addEventListener('click', () => {
  current++;
  if (current < sections.length) {
    sections[current].style.display = 'block';
  }
  if (current === sections.length - 1) {
    nextBtn.style.display = 'none';
    choice.style.display = 'block';
  }
});

// 音樂控制
const music = document.getElementById('bgm');
const musicBtn = document.getElementById('musicBtn');
let playing = false;
musicBtn.addEventListener('click', () => {
  if (!playing) {
    music.play();
    musicBtn.textContent = '🎵 暫停音樂';
    playing = true;
  } else {
    music.pause();
    musicBtn.textContent = '🎵 播放音樂';
    playing = false;
  }
});

// 願意按鈕 → 紀念畫面
const agreeBtns = document.querySelectorAll('.agree');
const card = document.querySelector('.card');
const celebrate = document.getElementById('celebrate');

agreeBtns.forEach(btn => {
  btn.addEventListener('click', () => {
    card.style.display = 'none';
    celebrate.style.display = 'block';

    // 星光粒子
    for(let i=0;i<50;i++){
      const star = document.createElement('div');
      star.classList.add('star');
      star.style.left = Math.random()*100 + '%';
      star.style.top = Math.random()*50 + 'px';
      star.style.width = star.style.height = (4+Math.random()*4) + 'px';
      star.style.animationDuration = (3 + Math.random()*2) + 's';
      document.body.appendChild(star);
    }

    // 心形淡入
    const heart = document.querySelector('.heart');
    heart.style.opacity = '1';

    // 簡單煙火爆炸
    function createFirework() {
      const x = Math.random() * window.innerWidth;
      const y = Math.random() * 200 + 50;
      const color = `hsl(${Math.random()*360}, 100%, 70%)`;
      for(let i=0;i<20;i++){
        const p = document.createElement('div');
        p.className = 'firework-particle';
        p.style.left = x+'px';
        p.style.top = y+'px';
        p.style.width = p.style.height = '6px';
        p.style.background = color;
        document.body.appendChild(p);
        const angle = Math.random()*2*Math.PI;
        const speed = 1 + Math.random()*3;
        let opacity = 1;
        let px = x, py = y;
        const interval = setInterval(()=>{
          px += Math.cos(angle)*speed;
          py += Math.sin(angle)*speed;
          opacity -= 0.03;
          p.style.left = px+'px';
          p.style.top = py+'px';
          p.style.opacity = opacity;
          if(opacity <= 0){
            clearInterval(interval);
            p.remove();
          }
        }, 30);
      }
    }
    setInterval(createFirework, 500);
  });
});
</script>

</body>
</html>
