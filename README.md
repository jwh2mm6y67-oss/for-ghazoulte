# for-ghazoute
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>For Ghazal ❤️</title>
  <style>
    :root {
      --bg-color: #fff0f3;
      --card-bg: #ffffff;
      --primary-color: #ff4d6d;
      --text-color: #590d22;
      --accent-color: #c9184a;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-color);
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      overflow: hidden;
      position: relative;
    }

    /* Floating Background Hearts */
    .heart {
      position: absolute;
      color: var(--primary-color);
      opacity: 0.2;
      font-size: 1.5rem;
      animation: float 8s infinite linear;
      z-index: 0;
    }

    @keyframes float {
      0% { transform: translateY(100vh) rotate(0deg); opacity: 0.2; }
      100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
    }

    /* Presentation Container */
    .container {
      width: 90%;
      max-width: 500px;
      height: 550px;
      position: relative;
      z-index: 1;
    }

    .slide {
      background: var(--card-bg);
      border-radius: 20px;
      padding: 2.5rem 2rem;
      box-shadow: 0 10px 30px rgba(255, 77, 109, 0.15);
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      opacity: 0;
      visibility: hidden;
      transition: opacity 0.6s ease, transform 0.6s ease;
      transform: scale(0.95);
    }

    .slide.active {
      opacity: 1;
      visibility: visible;
      transform: scale(1);
    }

    h1, h2 {
      color: var(--accent-color);
      margin-bottom: 1.2rem;
      font-weight: 700;
    }

    p {
      line-height: 1.6;
      font-size: 1.05rem;
      margin-bottom: 1rem;
      white-space: pre-line;
    }

    .divider {
      width: 50px;
      height: 3px;
      background-color: var(--primary-color);
      margin: 1rem auto;
      border-radius: 2px;
    }

    /* Buttons */
    .btn {
      background-color: var(--primary-color);
      color: white;
      border: none;
      padding: 0.8rem 1.8rem;
      font-size: 1rem;
      font-weight: 600;
      border-radius: 25px;
      cursor: pointer;
      margin-top: 1.5rem;
      transition: background 0.3s ease, transform 0.2s ease;
      box-shadow: 0 4px 15px rgba(255, 77, 109, 0.3);
    }

    .btn:hover {
      background-color: var(--accent-color);
      transform: translateY(-2px);
    }

    /* Final Slide Interactive Area */
    .question-box {
      width: 100%;
      height: 120px;
      position: relative;
      margin-top: 1rem;
    }

    #yes-btn {
      position: absolute;
      left: 20%;
      transform: translateX(-50%);
      background-color: #2ec4b6;
      box-shadow: 0 4px 15px rgba(46, 196, 182, 0.3);
    }

    #yes-btn:hover {
      background-color: #0f9f90;
    }

    #no-btn {
      position: absolute;
      right: 10%;
      background-color: #ff4d6d;
      transition: transform 0.1s ease, font-size 0.2s ease, opacity 0.2s ease;
      white-space: nowrap;
    }

    /* Celebration Screen */
    .celebration {
      display: none;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }

    .celebration h1 {
      font-size: 2.2rem;
      color: var(--accent-color);
    }
  </style>
</head>
<body>

  <!-- Floating Hearts Background -->
  <div id="hearts-container"></div>

  <div class="container">
    
    <!-- Slide 1 -->
    <div class="slide active" id="slide-1">
      <h1>Can I Steal a Minute?</h1>
      <p>Ghazal,</p>
      <p>Can I take just a minute of your time?</p>
      <p>I promise this one is worth reading until the end. ❤️</p>
      <button class="btn" onclick="nextSlide(2)">Next ✨</button>
    </div>

    <!-- Slide 2 -->
    <div class="slide" id="slide-2">
      <h2>Somehow, You Became Important</h2>
      <p>It hasn’t been that long since we met…

But somehow, it has been long enough for me to realize how much I’ve started feeling for you.

All the calls. All the chats.
The random reels & TikToks we send each other.
The little conversations that somehow make my day better.

It’s crazy how someone can enter your life so recently…
and already feel like they’ve been there for much longer.</p>
      <button class="btn" onclick="nextSlide(3)">Continue ❤️</button>
    </div>

    <!-- Slide 3 -->
    <div class="slide" id="slide-3">
      <h2>The Little Things</h2>
      <p>I don’t think I can properly explain how much I love you.
But I know I love the little things about you.

I love hearing your voice.
I love when you call me Hashoun or Hassoune.
I love your little habits, your way of talking, and even your breath when you fall asleep on the call.

And I notice the effort you make for me.
Maybe you don’t realize how much those little things mean to me… but I do.

I notice. I appreciate. And I love you for them. ❤️</p>
      <button class="btn" onclick="nextSlide(4)">Next 🌹</button>
    </div>

    <!-- Slide 4 -->
    <div class="slide" id="slide-4">
      <h2>You Changed Something In Me</h2>
      <p>You know I live away from my parents.
It’s just me and my sister, and honestly… sometimes it gets lonely.

For a long time, I prayed that one day I would meet someone who would make that loneliness feel a little less heavy.

Then you came into my life.
And somehow, things started feeling different.

You gave me something to look forward to.
Someone I want to talk to, hear from, and someone who makes an ordinary day feel special.</p>
      <button class="btn" onclick="nextSlide(5)">One last thing… ✨</button>
    </div>

    <!-- Slide 5 -->
    <div class="slide" id="slide-5">
      <h2>So, Ghazal…</h2>
      <p>I could keep writing about you…</p>
      <p>But I think there’s only one thing left to ask.</p>
      <h1 style="margin-top: 1rem; font-size: 1.5rem;">Will you be my girlfriend? ❤️</h1>
      
      <div class="question-box" id="q-box">
        <button class="btn" id="yes-btn" onclick="acceptProposal()">YES!<br><small style="font-weight:normal;">I’d love to.</small></button>
        <button class="btn" id="no-btn" onmouseover="runAway()" onclick="shrinkNo()">NO<br><small style="font-weight:normal;">…nice try. 😏</small></button>
      </div>
    </div>

    <!-- Final Success Slide -->
    <div class="slide celebration" id="slide-success">
      <h1>YAY! 🎉❤️</h1>
      <p style="font-size: 1.3rem; margin-top: 1rem;">I knew you'd say yes! 😉</p>
      <p>You just made me the happiest person alive, Ghazal.</p>
    </div>

  </div>

  <script>
    // Slide Navigation
    function nextSlide(slideNumber) {
      document.querySelectorAll('.slide').forEach(slide => {
        slide.classList.remove('active');
      });
      document.getElementById(`slide-${slideNumber}`).classList.add('active');
    }

    // Interactive Running/Shrinking NO Button Logic
    let noScale = 1;
    let clickCount = 0;

    function runAway() {
      const btn = document.getElementById('no-btn');
      const box = document.getElementById('q-box');
      
      // Calculate random positions within the question box bounds
      const maxX = box.clientWidth - btn.clientWidth;
      const maxY = box.clientHeight - btn.clientHeight;

      const randomX = Math.max(0, Math.floor(Math.random() * maxX));
      const randomY = Math.max(-50, Math.floor(Math.random() * maxY)); // Allow slight upward offset

      btn.style.left = `${randomX}px`;
      btn.style.top = `${randomY}px`;
    }

    function shrinkNo() {
      const btn = document.getElementById('no-btn');
      clickCount++;
      noScale -= 0.25;

      if (noScale <= 0.1) {
        btn.style.display = 'none'; // Disappears completely after enough clicks
      } else {
        btn.style.transform = `scale(${noScale})`;
      }
      
      // Also make it teleport on click
      runAway();
    }

    function acceptProposal() {
      document.querySelectorAll('.slide').forEach(slide => {
        slide.classList.remove('active');
      });
      document.getElementById('slide-success').classList.add('active');
      createHeartBurst();
    }

    // Ambient Hearts Generation
    function createHearts() {
      const container = document.getElementById('hearts-container');
      for (let i = 0; i < 15; i++) {
        const heart = document.createElement('div');
        heart.classList.add('heart');
        heart.innerHTML = '❤️';
        heart.style.left = `${Math.random() * 100}vw`;
        heart.style.animationDuration = `${5 + Math.random() * 5}s`;
        heart.style.animationDelay = `${Math.random() * 5}s`;
        container.appendChild(heart);
      }
    }

    // Confetti/Heart Burst on "YES"
    function createHeartBurst() {
      const container = document.getElementById('hearts-container');
      for (let i = 0; i < 50; i++) {
        const heart = document.createElement('div');
        heart.classList.add('heart');
        heart.innerHTML = '💖';
        heart.style.left = `${Math.random() * 100}vw`;
        heart.style.opacity = '1';
        heart.style.animationDuration = `${2 + Math.random() * 3}s`;
        container.appendChild(heart);
      }
    }

    createHearts();
  </script>
</body>
</html>
