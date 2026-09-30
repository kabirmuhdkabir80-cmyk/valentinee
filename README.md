<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0" />
  <title>For Khadijah 💗</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:ital,wght@0,400;0,500;0,600;1,400&family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --blush: #ffb6c1;
      --rose: #ff8fab;
      --deep-rose: #e85a8b;
      --text: #5c3a4a;
      --text-soft: #8b5a6b;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    html, body {
      height: 100%;
      overflow-x: hidden;
    }

    body {
      min-height: 100vh;
      background: linear-gradient(160deg, #fff0f5 0%, #ffe4ec 40%, #ffd6e7 100%);
      font-family: 'Poppins', sans-serif;
      color: var(--text);
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
    }

    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background: 
        radial-gradient(ellipse 80% 60% at 15% 25%, rgba(255,182,193,0.4) 0%, transparent 55%),
        radial-gradient(ellipse 70% 50% at 85% 75%, rgba(255,105,180,0.22) 0%, transparent 55%);
      pointer-events: none;
      z-index: 0;
    }

    /* Floating hearts */
    #hearts {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 1;
      overflow: hidden;
    }

    .heart {
      position: absolute;
      font-size: 14px;
      opacity: 0;
      animation: floatUp linear infinite;
      filter: drop-shadow(0 0 5px rgba(255,105,180,0.45));
    }

    @keyframes floatUp {
      0%   { transform: translateY(100vh) rotate(0deg) scale(0.5); opacity: 0; }
      12%  { opacity: 0.75; }
      90%  { opacity: 0.5; }
      100% { transform: translateY(-12vh) rotate(360deg) scale(1); opacity: 0; }
    }

    .petal {
      position: absolute;
      width: 11px;
      height: 15px;
      background: linear-gradient(135deg, #ffb6c1, #ff8fab);
      border-radius: 50% 0 50% 50%;
      opacity: 0.55;
      animation: petalFall linear infinite;
    }

    @keyframes petalFall {
      0%   { transform: translateY(-8vh) rotate(0deg); opacity: 0; }
      15%  { opacity: 0.65; }
      100% { transform: translateY(110vh) rotate(680deg) translateX(30px); opacity: 0; }
    }

    /* Page container */
    .page {
      position: relative;
      z-index: 10;
      width: 100%;
      max-width: 520px;
      padding: 20px;
    }

    /* Screens */
    .screen {
      width: 100%;
      text-align: center;
      transition: opacity 0.7s ease, transform 0.7s ease;
    }

    .screen.hidden {
      display: none !important;
    }

    /* ===== OPENING ===== */
    #opening {
      animation: fadeIn 1.1s ease-out;
    }

    .opening-title {
      font-family: 'Great Vibes', cursive;
      font-size: clamp(2.9rem, 9vw, 4.3rem);
      color: var(--deep-rose);
      text-shadow: 0 2px 22px rgba(232,90,139,0.28);
      margin-bottom: 14px;
      animation: softPulse 3.2s ease-in-out infinite;
    }

    .opening-sub {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(1.15rem, 3.5vw, 1.4rem);
      font-style: italic;
      color: var(--text-soft);
      margin-bottom: 42px;
      opacity: 0;
      animation: fadeInUp 0.9s ease 0.5s forwards;
    }

    /* Buttons */
    .btn {
      font-family: 'Poppins', sans-serif;
      font-weight: 500;
      font-size: 1rem;
      letter-spacing: 0.4px;
      border: none;
      cursor: pointer;
      border-radius: 50px;
      padding: 16px 36px;
      transition: all 0.35s cubic-bezier(0.34, 1.56, 0.64, 1);
    }

    .btn-primary {
      background: linear-gradient(135deg, #ff8fab, #e85a8b);
      color: white;
      box-shadow: 0 8px 28px rgba(232,90,139,0.42);
    }

    .btn-primary:hover {
      transform: translateY(-3px) scale(1.04);
      box-shadow: 0 12px 36px rgba(232,90,139,0.52);
    }

    .btn-yes {
      background: linear-gradient(135deg, #ff8fab, #e85a8b);
      color: white;
      box-shadow: 0 8px 28px rgba(232,90,139,0.4);
      min-width: 180px;
    }

    .btn-yes:hover {
      transform: translateY(-3px) scale(1.04);
    }

    .btn-think {
      background: rgba(255,255,255,0.8);
      color: var(--text-soft);
      border: 1.5px solid rgba(232,90,139,0.35);
      min-width: 170px;
      transition: all 0.35s cubic-bezier(0.34, 1.56, 0.64, 1);
    }

    .btn-think:hover {
      background: #fff0f5;
      border-color: var(--rose);
      color: var(--deep-rose);
    }

    .btn-next {
      background: linear-gradient(135deg, #ff8fab, #e85a8b);
      color: white;
      box-shadow: 0 6px 22px rgba(232,90,139,0.35);
      padding: 12px 28px;
      font-size: 0.95rem;
      margin-top: 8px;
    }

    .btn-next:hover {
      transform: translateY(-2px) scale(1.03);
      box-shadow: 0 10px 28px rgba(232,90,139,0.45);
    }

    /* ===== INVITATION CARD ===== */
    .card {
      background: rgba(255,255,255,0.78);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
      border-radius: 28px;
      padding: 42px 30px 48px;
      box-shadow: 0 20px 60px rgba(232,90,139,0.14),
                  0 8px 24px rgba(255,182,193,0.18),
                  inset 0 1px 0 rgba(255,255,255,0.85);
      border: 1px solid rgba(255,192,203,0.55);
      position: relative;
      overflow: hidden;
    }

    .card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 3px;
      background: linear-gradient(90deg, transparent, var(--rose), var(--deep-rose), var(--rose), transparent);
    }

    .rose-top {
      font-size: 1.85rem;
      margin-bottom: 10px;
      opacity: 0.9;
    }

    .invite-greeting {
      font-family: 'Great Vibes', cursive;
      font-size: clamp(1.85rem, 5.8vw, 2.55rem);
      color: var(--deep-rose);
      line-height: 1.3;
      margin-bottom: 16px;
    }

    .invite-question {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(1.12rem, 3.4vw, 1.32rem);
      font-style: italic;
      color: var(--text);
      line-height: 1.5;
      margin-bottom: 26px;
    }

    .details-box {
      background: linear-gradient(135deg, rgba(255,240,245,0.95), rgba(255,228,236,0.75));
      border-radius: 18px;
      padding: 18px 14px;
      margin: 0 auto 26px;
      max-width: 270px;
      border: 1px solid rgba(255,182,193,0.5);
    }

    .detail-line {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      font-size: 0.95rem;
      font-weight: 500;
      letter-spacing: 0.7px;
      padding: 5px 0;
    }

    /* ===== Sequential Flip Tabs ===== */
    .flip-container {
      margin: 0 auto 28px;
      max-width: 340px;
      min-height: 110px;
      position: relative;
    }

    .flip-tab {
      background: rgba(255,255,255,0.72);
      border: 1px solid rgba(255,182,193,0.55);
      border-radius: 16px;
      padding: 18px 16px;
      text-align: center;
      box-shadow: 0 4px 14px rgba(232,90,139,0.08);
      display: none;
      animation: fadeInUp 0.5s ease;
    }

    .flip-tab.active {
      display: block;
    }

    .flip-tab-text {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.08rem;
      font-style: italic;
      color: var(--text);
      line-height: 1.5;
    }

    .flip-progress {
      font-family: 'Poppins', sans-serif;
      font-size: 0.78rem;
      color: var(--text-soft);
      margin-top: 10px;
      letter-spacing: 0.5px;
    }

    .romantic-msg {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(1.05rem, 3vw, 1.18rem);
      font-style: italic;
      color: var(--text-soft);
      line-height: 1.65;
      margin-bottom: 12px;
    }

    .romantic-msg-2 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(1rem, 2.8vw, 1.12rem);
      color: var(--deep-rose);
      margin-bottom: 34px;
      font-weight: 500;
    }

    .final-q {
      font-family: 'Great Vibes', cursive;
      font-size: clamp(1.7rem, 5.4vw, 2.25rem);
      color: var(--deep-rose);
      margin-bottom: 28px;
      line-height: 1.25;
    }

    .buttons-row {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      justify-content: center;
      align-items: center;
      min-height: 58px;
      position: relative;
    }

    /* After flips content (hidden until last flip) */
    .after-flips {
      display: none;
    }

    .after-flips.show {
      display: block;
      animation: fadeInUp 0.6s ease;
    }

    /* ===== SUCCESS ===== */
    .yay {
      font-family: 'Great Vibes', cursive;
      font-size: clamp(3.1rem, 10vw, 4.6rem);
      color: var(--deep-rose);
      text-shadow: 0 4px 24px rgba(232,90,139,0.32);
      margin-bottom: 8px;
      animation: bounceIn 0.85s cubic-bezier(0.34, 1.56, 0.64, 1);
    }

    .its-date {
      font-family: 'Playfair Display', serif;
      font-size: clamp(1.25rem, 4vw, 1.55rem);
      margin-bottom: 18px;
      font-weight: 500;
    }

    .date-pill {
      font-size: 1.05rem;
      font-weight: 500;
      letter-spacing: 1.4px;
      color: var(--deep-rose);
      background: linear-gradient(135deg, rgba(255,240,245,0.95), rgba(255,228,236,0.85));
      display: inline-block;
      padding: 12px 28px;
      border-radius: 50px;
      margin-bottom: 26px;
      border: 1px solid rgba(255,182,193,0.5);
    }

    .looking {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(1.15rem, 3.4vw, 1.32rem);
      font-style: italic;
      color: var(--text-soft);
      line-height: 1.55;
    }

    .success-extra {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(1.05rem, 3vw, 1.2rem);
      font-style: italic;
      color: var(--text-soft);
      line-height: 1.6;
      margin-top: 18px;
      margin-bottom: 8px;
    }

    .success-heart {
      font-family: 'Great Vibes', cursive;
      font-size: clamp(1.4rem, 4vw, 1.7rem);
      color: var(--deep-rose);
      margin-top: 14px;
    }

    /* Music button */
    #music-btn {
      position: fixed;
      bottom: 22px;
      right: 22px;
      z-index: 100;
      width: 48px;
      height: 48px;
      border-radius: 50%;
      border: 1.5px solid rgba(232,90,139,0.4);
      background: rgba(255,255,255,0.88);
      backdrop-filter: blur(10px);
      cursor: pointer;
      font-size: 1.2rem;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 4px 16px rgba(232,90,139,0.2);
      transition: transform 0.3s;
    }

    #music-btn:hover { transform: scale(1.08); }

    /* Celebration particles */
    .burst {
      position: fixed;
      pointer-events: none;
      z-index: 50;
      font-size: 20px;
      animation: burstOut 2.6s ease-out forwards;
    }

    @keyframes burstOut {
      0%   { transform: translate(0,0) scale(0.3) rotate(0deg); opacity: 1; }
      100% { transform: translate(var(--x), var(--y)) scale(1.15) rotate(var(--r)); opacity: 0; }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(18px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(16px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    @keyframes softPulse {
      0%, 100% { transform: scale(1); }
      50%      { transform: scale(1.025); }
    }

    @keyframes bounceIn {
      0%   { transform: scale(0.25); opacity: 0; }
      60%  { transform: scale(1.1); }
      100% { transform: scale(1); opacity: 1; }
    }

    @media (max-width: 420px) {
      .card { padding: 32px 20px 40px; }
      .buttons-row { flex-direction: column; }
      .btn-yes, .btn-think { width: 100%; max-width: 260px; }
    }
  </style>
</head>
<body>

  <div id="hearts"></div>

  <button id="music-btn" title="Toggle music">🎵</button>
  <audio id="bg-music" loop preload="none">
    <!-- Optional soft track. Replace the src if you want a different song. -->
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
  </audio>

  <div class="page">

    <!-- OPENING SCREEN -->
    <section id="opening" class="screen">
      <div class="opening-title">Hey Khadijah… ❤️</div>
      <p class="opening-sub">I have something a little special for you.</p>
      <button class="btn btn-primary" id="open-btn">Open it 💗</button>
    </section>

    <!-- INVITATION SCREEN -->
    <section id="invitation" class="screen hidden">
      <div class="card">
        <div class="rose-top">🌹</div>
        <h1 class="invite-greeting">Khadijah, I’d really love to spend some time with you.</h1>
        <p class="invite-question">So… would you let me steal a few hours of your Wednesday night?</p>

        <div class="details-box">
          <div class="detail-line"><span>🌸</span> WEDNESDAY NIGHT</div>
          <div class="detail-line"><span>🕣</span> 8:30 PM</div>
          <div class="detail-line"><span>💗</span> JUST YOU &amp; ME</div>
        </div>

        <!-- ===== Sequential 5 flips ===== -->
        <div class="flip-container">
          <div class="flip-tab active" data-index="0">
            <div class="flip-tab-text">Clear your head after surviving those exams😭😭</div>
          </div>
          <div class="flip-tab" data-index="1">
            <div class="flip-tab-text">Get some fresh air, laugh a little and forget school for a minute</div>
          </div>
          <div class="flip-tab" data-index="2">
            <div class="flip-tab-text">Fresh air + Good vibes😎</div>
          </div>
          <div class="flip-tab" data-index="3">
            <div class="flip-tab-text">And obviously... enjoy some unnecessarily good company with me🌙❤️</div>
          </div>
          <div class="flip-tab" data-index="4">
            <div class="flip-tab-text">And who knows, Abdoul might make your night a little better🤭😊❤️🤏</div>
          </div>
          <div class="flip-progress" id="flip-progress">1 / 5</div>
          <button class="btn btn-next" id="next-flip-btn">Next 💗</button>
        </div>
        <!-- ===== END sequential flips ===== -->

        <div class="after-flips" id="after-flips">
          <p class="romantic-msg">Nothing too complicated. Just good conversation, some laughs, a nice evening… and hopefully your beautiful company.</p>
          <p class="romantic-msg-2">I think Wednesday would be a little better with you there.</p>

          <h2 class="final-q">So Khadijah… will you hang out with me? 💗</h2>

          <div class="buttons-row" id="btn-row">
            <button class="btn btn-yes" id="yes-btn">YES, OF COURSE 💕</button>
            <button class="btn btn-think" id="think-btn">LET ME THINK 👀</button>
          </div>
        </div>
      </div>
    </section>

    <!-- SUCCESS SCREEN -->
    <section id="success" class="screen hidden">
      <div class="card">
        <div class="yay">YAYYY 💗</div>
        <p class="its-date">It’s a date then.</p>
        <div class="date-pill">Wednesday • 8:30 PM</div>
        <p class="looking">I’m looking forward to seeing you, Khadijah. ❤️</p>
        <p class="success-extra">I can’t wait to walk beside you, hear your laugh, and make this Wednesday night feel a little softer… just for us.</p>
        <p class="success-heart">Until then… I’ll be counting the hours 🌙💕</p>
      </div>
    </section>

  </div>

  <script>
    // ===== Floating hearts & petals =====
    const heartsEl = document.getElementById('hearts');
    const emojis = ['💗', '💕', '💖', '🌸', '✨', '🤍', '🌹'];

    function spawnHeart() {
      const el = document.createElement('div');
      el.className = 'heart';
      el.textContent = emojis[Math.floor(Math.random() * emojis.length)];
      el.style.left = Math.random() * 100 + 'vw';
      el.style.fontSize = (11 + Math.random() * 13) + 'px';
      el.style.animationDuration = (8 + Math.random() * 9) + 's';
      heartsEl.appendChild(el);
      setTimeout(() => el.remove(), 17000);
    }

    function spawnPetal() {
      const el = document.createElement('div');
      el.className = 'petal';
      el.style.left = Math.random() * 100 + 'vw';
      el.style.animationDuration = (11 + Math.random() * 10) + 's';
      heartsEl.appendChild(el);
      setTimeout(() => el.remove(), 21000);
    }

    for (let i = 0; i < 10; i++) setTimeout(spawnHeart, i * 350);
    setInterval(spawnHeart, 850);
    setInterval(spawnPetal, 1300);

    // ===== Screen switching (robust) =====
    const opening   = document.getElementById('opening');
    const invitation = document.getElementById('invitation');
    const success   = document.getElementById('success');

    function showScreen(toShow) {
      // Hide all
      [opening, invitation, success].forEach(s => {
        s.classList.add('hidden');
        s.style.opacity = '';
        s.style.transform = '';
      });
      // Show target
      toShow.classList.remove('hidden');
      // Trigger reflow then fade in
      void toShow.offsetWidth;
      toShow.style.opacity = '0';
      toShow.style.transform = 'translateY(20px)';
      requestAnimationFrame(() => {
        toShow.style.transition = 'opacity 0.75s ease, transform 0.75s ease';
        toShow.style.opacity = '1';
        toShow.style.transform = 'translateY(0)';
      });
    }

    // Open button
    document.getElementById('open-btn').addEventListener('click', () => {
      showScreen(invitation);
    });

    // Yes button
    document.getElementById('yes-btn').addEventListener('click', () => {
      createBurst();
      setTimeout(() => showScreen(success), 400);
    });

    // ===== Sequential flips =====
    let currentFlip = 0;
    const flipTabs = document.querySelectorAll('.flip-tab');
    const nextFlipBtn = document.getElementById('next-flip-btn');
    const flipProgress = document.getElementById('flip-progress');
    const afterFlips = document.getElementById('after-flips');

    nextFlipBtn.addEventListener('click', () => {
      flipTabs[currentFlip].classList.remove('active');
      currentFlip++;

      if (currentFlip < flipTabs.length) {
        flipTabs[currentFlip].classList.add('active');
        flipProgress.textContent = (currentFlip + 1) + ' / 5';
        if (currentFlip === flipTabs.length - 1) {
          nextFlipBtn.textContent = 'Continue 💕';
        }
      } else {
        // Hide flip UI and show the rest
        document.querySelector('.flip-container').style.display = 'none';
        afterFlips.classList.add('show');
      }
    });

    // ===== Playful "Let me think" =====
    const thinkBtn = document.getElementById('think-btn');
    const messages = [
      "Are you sure? 🥺",
      "I think you know the answer 😌💕",
      "Pretty please? 💗",
      "Just say yes… 😊",
      "You already know 💕",
      "Come on… 🥺❤️"
    ];
    let thinkCount = 0;

    thinkBtn.addEventListener('click', () => {
      thinkCount++;
      const idx = Math.min(thinkCount - 1, messages.length - 1);
      thinkBtn.textContent = messages[idx];

      // Move playfully
      const x = (Math.random() - 0.5) * 120;
      const y = (Math.random() - 0.5) * 50;
      thinkBtn.style.transform = `translate(${x}px, ${y}px)`;
    });

    // ===== Celebration burst =====
    function createBurst() {
      for (let i = 0; i < 42; i++) {
        setTimeout(() => {
          const p = document.createElement('div');
          p.className = 'burst';
          p.textContent = emojis[Math.floor(Math.random() * emojis.length)];
          p.style.left = '50%';
          p.style.top = '42%';
          const angle = Math.random() * Math.PI * 2;
          const dist = 70 + Math.random() * 200;
          p.style.setProperty('--x', Math.cos(angle) * dist + 'px');
          p.style.setProperty('--y', Math.sin(angle) * dist - 30 + 'px');
          p.style.setProperty('--r', (Math.random() * 600 - 300) + 'deg');
          p.style.fontSize = (15 + Math.random() * 16) + 'px';
          document.body.appendChild(p);
          setTimeout(() => p.remove(), 2800);
        }, i * 30);
      }
    }

    // ===== Music =====
    const musicBtn = document.getElementById('music-btn');
    const music = document.getElementById('bg-music');
    music.volume = 0.25;
    let playing = false;

    musicBtn.addEventListener('click', () => {
      if (playing) {
        music.pause();
        musicBtn.textContent = '🎵';
      } else {
        music.play().catch(() => {});
        musicBtn.textContent = '🔇';
      }
      playing = !playing;
    });
  </script>
</body>
</html>
