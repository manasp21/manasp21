<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: #000;
            color: #FFE81F;
            font-family: 'Orbitron', 'Courier New', monospace;
            overflow-x: hidden;
            height: 100vh;
        }
        
        .starfield {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #000;
            z-index: -1;
        }
        
        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: white;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }
        
        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }
        
        .opening-text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            font-size: 18px;
            animation: fade-in-out 6s forwards;
        }
        
        @keyframes fade-in-out {
            0% { opacity: 0; }
            20% { opacity: 1; }
            80% { opacity: 1; }
            100% { opacity: 0; }
        }
        
        .logo {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 48px;
            font-weight: bold;
            text-align: center;
            animation: logo-zoom 4s 6s forwards;
            opacity: 0;
        }
        
        @keyframes logo-zoom {
            0% { opacity: 0; transform: translate(-50%, -50%) scale(0.1); }
            50% { opacity: 1; transform: translate(-50%, -50%) scale(1.2); }
            100% { opacity: 1; transform: translate(-50%, -50%) scale(1); }
        }
        
        .crawl-container {
            position: absolute;
            top: 100%;
            left: 50%;
            transform: translateX(-50%);
            width: 80%;
            animation: crawl 20s 10s forwards;
            opacity: 0;
        }
        
        @keyframes crawl {
            0% { opacity: 0; top: 100%; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { opacity: 0; top: -50%; }
        }
        
        .crawl-text {
            font-size: 20px;
            line-height: 1.8;
            text-align: justify;
            perspective: 400px;
            transform: rotateX(25deg);
        }
        
        .space-scene {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100vh;
            animation: scene-fade-in 2s 30s forwards;
            opacity: 0;
        }
        
        @keyframes scene-fade-in {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
        
        .death-star {
            position: absolute;
            top: 10%;
            right: -50%;
            font-family: 'Courier New', monospace;
            font-size: 12px;
            line-height: 1;
            color: #888;
            animation: death-star-approach 15s 32s infinite;
        }
        
        @keyframes death-star-approach {
            0% { right: -50%; transform: scale(0.5) rotate(0deg); }
            50% { right: 20%; transform: scale(1) rotate(180deg); }
            100% { right: -50%; transform: scale(0.5) rotate(360deg); }
        }
        
        .star-destroyer {
            position: absolute;
            top: 60%;
            left: -100%;
            font-family: 'Courier New', monospace;
            font-size: 10px;
            line-height: 1;
            color: #666;
            animation: destroyer-flyby 12s 40s infinite;
        }
        
        @keyframes destroyer-flyby {
            0% { left: -100%; transform: scale(0.8); }
            50% { left: 50%; transform: scale(1.2); }
            100% { left: 120%; transform: scale(0.8); }
        }
        
        .millennium-falcon {
            position: absolute;
            top: 30%;
            left: -20%;
            font-family: 'Courier New', monospace;
            font-size: 8px;
            line-height: 1;
            color: #FFE81F;
            animation: falcon-escape 10s 50s infinite;
        }
        
        @keyframes falcon-escape {
            0% { left: -20%; top: 30%; transform: rotate(-10deg); }
            30% { left: 40%; top: 20%; transform: rotate(5deg); }
            60% { left: 80%; top: 35%; transform: rotate(-15deg); }
            100% { left: 120%; top: 25%; transform: rotate(10deg); }
        }
        
        .x-wing-squadron {
            position: absolute;
            top: 70%;
            left: -30%;
            font-family: 'Courier New', monospace;
            font-size: 6px;
            line-height: 1;
            color: #00FF00;
            animation: squadron-formation 14s 45s infinite;
        }
        
        @keyframes squadron-formation {
            0% { left: -30%; }
            100% { left: 130%; }
        }
        
        .welcome-message {
            position: absolute;
            bottom: 10%;
            left: 50%;
            transform: translateX(-50%);
            text-align: center;
            font-size: 24px;
            animation: message-appear 3s 60s forwards;
            opacity: 0;
        }
        
        @keyframes message-appear {
            0% { opacity: 0; transform: translateX(-50%) translateY(50px); }
            100% { opacity: 1; transform: translateX(-50%) translateY(0); }
        }
    </style>
</head>
<body>

<div class="starfield" id="starfield"></div>

<div class="opening-text">
    A long time ago in a galaxy far,<br>
    far away....
</div>

<div class="logo">
    MANAS<br>
    <span style="font-size: 24px;">SOFTWARE ENGINEER</span>
</div>

<div class="crawl-container">
    <div class="crawl-text">
        <p style="text-align: center; font-size: 24px; margin-bottom: 30px;">Episode I</p>
        <p style="text-align: center; font-size: 24px; margin-bottom: 50px;">THE DEVELOPER'S JOURNEY</p>
        
        <p>In a digital realm where code flows like the Force, a young developer has emerged from the shadows of learning to master the ancient arts of software engineering.</p>
        
        <p>Armed with the wisdom of countless algorithms and the power of clean code, they stand ready to face the challenges that lie ahead in the vast expanse of the programming universe.</p>
        
        <p>Their mission: to build applications that will bring balance to the digital galaxy and create solutions that will echo through the ages....</p>
    </div>
</div>

<div class="space-scene">
    <div class="death-star">
<pre>
                    .-.
                   /   \
                  |  O  |
                   \   /
               .-----'------.
             /               \
            |    .........    |
            |   :         :   |
            |   :    *    :   |
            |   :         :   |
            |    '.......'    |
             \               /
              '-.._______.-'
                    |
               .----+----.
              /           \
             |   .-""-.    |
             |  /       \   |
             | |    O    |  |
             |  \       /   |
             |   '-...-'    |
              \             /
               '-.______.-'
                    |
               .----+----.
              /           \
             |             |
             |      *      |
             |             |
              \           /
               '-.......-'
</pre>
    </div>
    
    <div class="star-destroyer">
<pre>
    /\                                           /\
   /  \                                         /  \
  /    \                                       /    \
 /      \________________           __________/      \
/                        \_   _   _/                 \
\                          \_/ \_/                   /
 \                          /   \                   /
  \                        /     \                 /
   \                      /       \               /
    \                    /         \             /
     \__________________/           \___________/
      |  |  |  |  |  |  |           |  |  |  |  |
      |  |  |  |  |  |  |           |  |  |  |  |
      |__|__|__|__|__|__|___________|__|__|__|__|
</pre>
    </div>
    
    <div class="millennium-falcon">
<pre>
         .-..-. 
        ( o   o )
         \  .  /
          |\_/|
      .--'     '--.
     /     ___     \
    |   .-'   '-.   |
    |  |  () ()  |  |
     \  \  ___  /  /
      '--\     /'--
         |  |  |
         |  |  |
        /   |   \
       '----+----'
</pre>
    </div>
    
    <div class="x-wing-squadron">
<pre>
  |-o-|    |-o-|    |-o-|    |-o-|
   \|/      \|/      \|/      \|/
    |        |        |        |
   /|\      /|\      /|\      /|\
  |-o-|    |-o-|    |-o-|    |-o-|
</pre>
    </div>
</div>

<div class="welcome-message">
    <h1>Welcome to My Repository</h1>
    <p style="font-style: italic; font-size: 18px;">May the Code be with you</p>
    <img src="image.png" alt="Hello There" width="200" style="margin-top: 20px; border-radius: 10px;">
</div>

<script>
// Create animated starfield
function createStarfield() {
    const starfield = document.getElementById('starfield');
    const numStars = 200;
    
    for (let i = 0; i < numStars; i++) {
        const star = document.createElement('div');
        star.className = 'star';
        star.style.left = Math.random() * 100 + '%';
        star.style.top = Math.random() * 100 + '%';
        star.style.animationDelay = Math.random() * 3 + 's';
        star.style.animationDuration = (Math.random() * 3 + 2) + 's';
        starfield.appendChild(star);
    }
}

// Initialize starfield when page loads
createStarfield();
</script>

</body>
</html>