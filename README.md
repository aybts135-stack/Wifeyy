# Wifeyy
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Universe - Happy Birthday Prachuuu!</title>
    <style>
        /* Base Styling & Full-screen Setup */
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            overflow: hidden; /* Crucial for flowing elements */
            font-family: 'Segoe UI', 'Roboto', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            background: radial-gradient(circle at center, #1b2735 0%, #090a0f 100%);
        }

        /* --- Universe Background Elements --- */
        .stars, .twinkle {
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            width: 100%; height: 100%;
            display: block;
        }

        .stars {
            background: transparent url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyIiBoZWlnaHQ9IjIiIHZpZXdCb3g9IjAgMCAyIDIiPjxjaXJjbGUgY3g9IjEiIGN5PSIxIiByPSIxIiBmaWxsPSIjRkZGIiBmaWxsLW9wYWNpdHk9IjAuNiIvPjwvc3ZnPg==') repeat top center;
            z-index: 0;
            opacity: 0.5;
        }

        .twinkle {
            background: transparent url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMTAiIGhlaWdodD0iMTEwIiB2aWV3Qm94PSIwIDAgMTEwIDExMCI+PGNpcmNsZSBjeD0iNTAiIGN5PSI1MCIgcj0iMSIgZmlsbD0iI0ZGRiIvPjxjaXJjbGUgY3g9IjEwMCIgY3k9IjEwMCIgcj0iMS41IiBmaWxsPSIjRkZGIi8+PC9zdmc+') repeat top center;
            z-index: 1;
            animation: move-twinkle 100s linear infinite;
        }

        @keyframes move-twinkle {
            from { background-position: 0 0; }
            to { background-position: -1000px 500px; }
        }

        /* --- Flowing Elements Styling --- */
        #flow-container {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            z-index: 2; /* Between background and card */
            pointer-events: none; /* Allows clicking through the items */
        }

        .floating-item {
            position: absolute;
            bottom: -50px; /* Start just below screen */
            font-size: 24px;
            opacity: 0.8;
            animation: floatUp linear infinite;
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }
            10% { opacity: 0.8; }
            90% { opacity: 0.8; }
            100% {
                transform: translateY(-110vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* --- The Main Pop-up Card (Glassmorphism) --- */
        #main-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            
            padding: 40px;
            border-radius: 25px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 15px 35px rgba(0,0,0,0.5);
            
            max-width: 420px;
            width: 90%;
            z-index: 10; /* Above flowing items */
            text-align: center;
            color: white;
            transition: all 0.5s ease;
        }

        h1 {
            color: #ff80ab;
            margin-bottom: 10px;
            text-shadow: 0 0 10px rgba(255, 128, 171, 0.5);
        }

        p {
            color: #e0e0e0;
            font-size: 1.1rem;
            line-height: 1.5;
        }

        /* --- Photos Setup --- */
        .photo-container {
            display: flex;
            gap: 15px;
            justify-content: center;
            margin: 25px 0;
        }

        .photo-container img {
            width: 90px;
            height: 90px;
            object-fit: cover;
            border-radius: 50%;
            border: 3px solid #ff80ab;
            box-shadow: 0 0 15px rgba(255, 128, 171, 0.3);
            transition: transform 0.3s ease;
        }

        .photo-container img:hover { transform: scale(1.1); }

        /* --- Buttons Setup --- */
        .btn-group {
            margin-top: 30px;
            position: relative;
            height: 60px;
        }

        button {
            padding: 12px 30px;
            font-size: 1rem;
            font-weight: bold;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            outline: none;
        }

        #yes-btn {
            background: linear-gradient(45deg, #ff4081, #d81b60);
            color: white;
            box-shadow: 0 4px 15px rgba(216, 27, 96, 0.4);
        }

        #yes-btn:hover {
            box-shadow: 0 6px 20px rgba(216, 27, 96, 0.6);
            transform: translateY(-2px);
        }

        #no-btn {
            background-color: rgba(255, 255, 255, 0.1);
            color: #ccc;
            border: 1px solid rgba(255, 255, 255, 0.2);
            position: absolute;
        }
    </style>
</head>
<body>

    <div class="stars"></div>
    <div class="twinkle"></div>

    <div id="flow-container"></div>

    <div id="main-card">
        <h1>Happy Birthday,<br>Prachuuu! 🎂🌠</h1>
        
        <div class="photo-container">
            <img src="photo1.jpg" alt="Memory 1">
            <img src="photo2.jpg" alt="Memory 2">
            <img src="photo3.jpg" alt="Memory 3">
        </div>

        <p>You brighten up my entire universe. ❤️</p>
        <p style="font-size: 1.2rem; color: #ff80ab;"><strong>Will you love being my<br>bestie and wifeyyy?</strong></p>

        <div class="btn-group">
            <button id="yes-btn" onclick="celebrate()">Yes, Forever! 💖</button>
            <button id="no-btn" onmouseover="moveButton()" onclick="moveButton()">No</button>
        </div>
    </div>

    <script>
        // --- 1. Flowing Elements System ---
        const flowContainer = document.getElementById('flow-container');
        // Define the items to float up
        const items = ['💜', '❤️', '💍', '🍫', '💖', '✨'];

        function createFloatingItem(isCelebration = false) {
            const item = document.createElement('div');
            item.classList.add('floating-item');
            
            // Pick random character
            item.innerText = items[Math.floor(Math.random() * items.length)];
            
            // Randomize horizontal position
            item.style.left = Math.random() * 100 + 'vw';
            
            // Randomize size slightly
            const size = Math.random() * (30 - 15) + 15; // 15px to 30px
            item.style.fontSize = size + 'px';

            // Randomize duration (speed)
            // Celebration items fall faster/float faster
            const duration = isCelebration 
                ? (Math.random() * (4 - 2) + 2)  // 2s to 4s
                : (Math.random() * (10 - 6) + 6); // 6s to 10s
            item.style.animationDuration = duration + 's';

            // Slight randomization of opacity
            item.style.opacity = Math.random() * (0.9 - 0.5) + 0.5;

            flowContainer.appendChild(item);

            // Remove element after animation finishes to keep memory usage low
            setTimeout(() => {
                item.remove();
            }, duration * 1000);
        }

        // Start slow, steady flow
        let flowInterval = setInterval(createFloatingItem, 500); // 1 item every 0.5s


        // --- 2. Interactive Buttons System ---
        function moveButton() {
            const btn = document.getElementById('no-btn');
            
            const padding = 20;
            const maxWidth = window.innerWidth - btn.clientWidth - padding;
            const maxHeight = window.innerHeight - btn.clientHeight - padding;
            
            let newX = Math.random() * maxWidth;
            let newY = Math.random() * maxHeight;

            btn.style.position = 'fixed';
            btn.style.left = newX + 'px';
            btn.style.top = newY + 'px';
            btn.style.zIndex = '1000';
        }

        function celebrate() {
            // A. Update the card
            const card = document.getElementById('main-card');
            card.style.background = "rgba(216, 27, 96, 0.85)";
            card.style.borderColor = "transparent";
            
            card.innerHTML = `
                <h1 style="font-size: 2.8rem; color: white; text-shadow: 0 0 15px rgba(255,255,255,0.7);">🎉 YAYYY! 🎉</h1>
                <p style="font-size: 1.3rem; color: white;">I am the luckiest person in the whole galaxy!</p>
                <p style="font-size: 1.1rem; color: white; margin-top: 10px;">Happy Birthday, Prachuuu! ❤️</p>
                <div style="font-size: 60px; margin-top: 20px;">💍 ✨ 🌸 🍫 ✨ ❤️</div>
            `;

            // B. Intensify the flowing elements (Celebration mode)
            clearInterval(flowInterval); // Stop slow flow
            flowInterval = setInterval(() => createFloatingItem(true), 50); // Create many faster items

            // Optional: slow back down after a few seconds
            setTimeout(() => {
                clearInterval(flowInterval);
                flowInterval = setInterval(createFloatingItem, 300); // slightly faster than original
            }, 5000);
        }
    </script>
</body>
</html>
