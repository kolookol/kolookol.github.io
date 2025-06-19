<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PACARKUUU LUCU</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background-color: #FFF5E6;
            margin: 0;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            overflow-x: hidden;
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
            position: relative;
            z-index: 100;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .header h1 {
            font-size: 2.5rem;
            color: #FF6B6B;
            margin-bottom: 5px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            background: linear-gradient(45deg, #ff9a9e, #fad0c4, #ff9a9e);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .header p {
            font-size: 1.2rem;
            color: #FF8E8E;
            margin-top: 0;
            font-weight: bold;
        }

        .polaroid-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            max-width: 900px;
            width: 100%;
            position: relative;
            z-index: 100;
            padding: 10px;
        }

        @media (max-width: 768px) {
            .polaroid-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 480px) {
            .polaroid-container {
                grid-template-columns: 1fr;
            }
        }

        .polaroid {
            background: white;
            padding: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            transform: rotate(var(--rotate));
            transition: all 0.3s ease;
            position: relative;
            border-radius: 5px;
        }

        .polaroid:nth-child(3n+1) { --rotate: 2deg; }
        .polaroid:nth-child(3n+2) { --rotate: -1deg; }
        .polaroid:nth-child(3n+3) { --rotate: 1deg; }

        .polaroid:hover {
            transform: rotate(0deg) scale(1.05);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
            z-index: 1;
        }

        .pushpin {
            position: absolute;
            top: 10px;
            right: 10px;
            width: 25px;
            height: 25px;
            background: #FF6B6B;
            border-radius: 50% 50% 0 50%;
            transform: rotate(45deg);
            z-index: 2;
            box-shadow: 1px 1px 3px rgba(0,0,0,0.3);
        }

        .pushpin::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 6px;
            height: 6px;
            background: white;
            border-radius: 50%;
            transform: translate(-50%, -50%);
        }

        .polaroid-img {
            width: 100%;
            height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            border-radius: 3px;
            border: 1px solid #f0f0f0;
        }

        .polaroid-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .polaroid:hover .polaroid-img img {
            transform: scale(1.05);
        }

        .signature {
            margin: 40px 0 20px;
            font-family: 'Dancing Script', cursive;
            font-size: 2.5rem;
            color: #FF6B6B;
            position: relative;
            z-index: 100;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            animation: pulse 1.5s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        .love {
            position: fixed;
            font-size: 24px;
            animation: float 3s ease-out forwards;
            pointer-events: none;
            z-index: 9999;
            user-select: none;
            filter: drop-shadow(0 0 5px rgba(255,64,129,0.7));
        }

        @keyframes float {
            0% {
                transform: translate(0, 0) rotate(0deg) scale(0.3);
                opacity: 1;
            }
            100% {
                transform: translate(var(--tx), var(--ty)) rotate(var(--rot)) scale(1);
                opacity: 0;
            }
        }

        .love-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            pointer-events: none;
            z-index: 9998;
            overflow: hidden;
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&display=swap" rel="stylesheet">
</head>
<body>
    <div class="love-container" id="loveContainer"></div>

    <div class="header">
        <h1>PACARKUUU LUCU</h1>
        <p>Elsa indahh safitrii ❤️</p>
    </div>

    <div class="polaroid-container">
        <!-- Row 1 -->
        <div class="polaroid">
            <div class="pushpin"></div>
            <div class="polaroid-img">
                <img src="IMG-20250619-WA0003.jpg" alt="Photo 1">
            </div>
        </div>

        <div class="polaroid">
            <div class="pushpin"></div>
            <div class="polaroid-img">
                <img src="IMG-20250619-WA0005.jpg" alt="Photo 2">
            </div>
        </div>

        <div class="polaroid">
            <div class="pushpin"></div>
            <div class="polaroid-img">
                <img src="WhatsApp Image 2025-06-19 at 18.19.29_51ab939a.jpg" alt="Photo 3">
            </div>
        </div>

        <!-- Row 2 -->
        <div class="polaroid">
            <div class="pushpin"></div>
            <div class="polaroid-img">
                <img src="WhatsApp Image 2025-06-19 at 18.19.29_927c137d.jpg" alt="Photo 4">
            </div>
        </div>

        <div class="polaroid">
            <div class="pushpin"></div>
            <div class="polaroid-img">
                <img src="IMG-20250619-WA0012.jpg" alt="Photo 5">
            </div>
        </div>

        <div class="polaroid">
            <div class="pushpin"></div>
            <div class="polaroid-img">
                <img src="IMG-20250619-WA0009.jpg" alt="Photo 6">
            </div>
        </div>
    </div>

    <div class="signature">I LOVEEE UU</div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const container = document.getElementById('loveContainer');
            const colors = ['#ff4081', '#ff79b0', '#ff5252', '#ff8a80', '#ff80ab'];
            const emojis = ['❤️', '🧡', '💛', '💚', '💙', '💜', '🤍', '💖', '💗', '💓', '💞', '💕'];
            
            function createExplosion(count, originX, originY) {
                for (let i = 0; i < count; i++) {
                    const heart = document.createElement('div');
                    heart.innerHTML = emojis[Math.floor(Math.random() * emojis.length)];
                    heart.classList.add('love');
                    
                    const size = Math.random() * 30 + 20;
                    const color = colors[Math.floor(Math.random() * colors.length)];
                    const angle = Math.random() * Math.PI * 2;
                    const distance = 150 + Math.random() * 300;
                    const tx = Math.cos(angle) * distance;
                    const ty = Math.sin(angle) * distance - 150;
                    const rotation = Math.random() * 720 - 360;
                    
                    heart.style.left = originX + 'px';
                    heart.style.top = originY + 'px';
                    heart.style.fontSize = size + 'px';
                    heart.style.color = color;
                    heart.style.setProperty('--tx', tx + 'px');
                    heart.style.setProperty('--ty', ty + 'px');
                    heart.style.setProperty('--rot', rotation + 'deg');
                    heart.style.animationDuration = (1 + Math.random() * 2) + 's';
                    
                    container.appendChild(heart);
                    setTimeout(() => heart.remove(), 3000);
                }
            }
            
            setTimeout(() => {
                createExplosion(150, window.innerWidth / 2, window.innerHeight / 2);
                setTimeout(() => {
                    createExplosion(50, window.innerWidth * 0.2, window.innerHeight * 0.3);
                    createExplosion(50, window.innerWidth * 0.8, window.innerHeight * 0.7);
                }, 300);
            }, 300);
            
            document.addEventListener('click', function(e) {
                createExplosion(30, e.clientX, e.clientY);
            });
        });
    </script>
</body>
</html>
