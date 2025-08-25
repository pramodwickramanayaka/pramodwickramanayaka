<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aruna Pramodh - Personal Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: #000000;
            min-height: 100vh;
            overflow-x: hidden;
        }

        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .particle {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .code-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
            overflow: hidden;
        }

        .code-line {
            position: absolute;
            color: rgba(0, 255, 0, 0.3);
            font-family: 'Courier New', monospace;
            font-size: 12px;
            white-space: nowrap;
            animation: codeScroll 15s linear infinite;
        }

        @keyframes codeScroll {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100vw); }
        }

        .matrix-rain {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .matrix-column {
            position: absolute;
            color: #00ff41;
            font-family: 'Courier New', monospace;
            font-size: 14px;
            opacity: 0.4;
            animation: matrixFall linear infinite;
        }

        @keyframes matrixFall {
            0% { transform: translateY(-100vh); }
            100% { transform: translateY(100vh); }
        }

        .binary-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
            opacity: 0.1;
        }

        .binary-digit {
            position: absolute;
            color: #00bcd4;
            font-family: 'Courier New', monospace;
            font-size: 16px;
            animation: binaryPulse 2s ease-in-out infinite;
        }

        @keyframes binaryPulse {
            0%, 100% { opacity: 0.1; }
            50% { opacity: 0.3; }
        }

        .container {
            position: relative;
            z-index: 2;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .header {
            text-align: center;
            padding: 80px 0;
            color: white;
        }

        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 30px;
            animation: pulse 2s ease-in-out infinite;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            overflow: hidden;
            padding: 10px;
        }

        .profile-img img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
        }

        .profile-img-fallback {
            font-size: 60px;
            font-weight: bold;
            color: white;
            display: none;
        }

        @keyframes pulse {
            0% { transform: scale(1); box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.4); }
            50% { transform: scale(1.05); box-shadow: 0 0 0 20px rgba(255, 255, 255, 0); }
            100% { transform: scale(1); box-shadow: 0 0 0 0 rgba(255, 255, 255, 0); }
        }

        .name {
            font-size: 3.5em;
            font-weight: bold;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: slideInFromTop 1s ease-out;
        }

        @keyframes slideInFromTop {
            0% { opacity: 0; transform: translateY(-50px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        .subtitle {
            font-size: 1.5em;
            opacity: 0.9;
            animation: slideInFromBottom 1s ease-out 0.5s both;
        }

        @keyframes slideInFromBottom {
            0% { opacity: 0; transform: translateY(50px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        .info-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            padding: 50px 0;
        }

        .card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            padding: 30px;
            color: white;
            text-align: center;
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease-out;
        }

        .card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 40px rgba(0,255,0,0.2);
            background: rgba(255, 255, 255, 0.15);
            border: 1px solid rgba(0, 255, 0, 0.3);
        }

        @keyframes fadeInUp {
            0% { opacity: 0; transform: translateY(30px); }
            100% { opacity: 1; transform: translateY(0); }
        }

        .card-icon {
            font-size: 3em;
            margin-bottom: 20px;
            display: block;
            color: #00ff41;
            text-shadow: 0 0 10px #00ff41;
            animation: iconGlow 2s ease-in-out infinite alternate;
        }

        @keyframes iconGlow {
            from { 
                color: #00ff41;
                text-shadow: 0 0 10px #00ff41, 0 0 20px #00ff41; 
            }
            to { 
                color: #4ecdc4;
                text-shadow: 0 0 10px #4ecdc4, 0 0 20px #4ecdc4; 
            }
        }

        .card h3 {
            font-size: 1.5em;
            margin-bottom: 15px;
            color: #fff;
        }

        .card p {
            font-size: 1.1em;
            opacity: 0.9;
            line-height: 1.6;
        }

        .floating-shapes {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .shape {
            position: absolute;
            opacity: 0.3;
            font-size: 2em;
            animation: floatShape 8s ease-in-out infinite;
            color: #00ff41;
        }

        .shape:nth-child(1) {
            top: 10%;
            left: 10%;
            animation-delay: 0s;
        }

        .shape:nth-child(2) {
            top: 20%;
            right: 10%;
            animation-delay: 2s;
        }

        .shape:nth-child(3) {
            bottom: 10%;
            left: 20%;
            animation-delay: 4s;
        }

        .shape:nth-child(4) {
            bottom: 20%;
            right: 20%;
            animation-delay: 6s;
        }

        @keyframes floatShape {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-30px) rotate(180deg); }
        }

        .contact-btn {
            display: inline-block;
            background: linear-gradient(45deg, #00ff41, #4ecdc4);
            color: black;
            padding: 15px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.2em;
            margin-top: 30px;
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(0,255,65,0.3);
        }

        .contact-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(0,255,65,0.5);
            background: linear-gradient(45deg, #4ecdc4, #00ff41);
        }

        @media (max-width: 768px) {
            .name { font-size: 2.5em; }
            .subtitle { font-size: 1.2em; }
            .info-cards { grid-template-columns: 1fr; }
            .header { padding: 50px 0; }
        }

        .glow-text {
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { 
                text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #00ff41; 
            }
            to { 
                text-shadow: 0 0 10px #fff, 0 0 20px #fff, 0 0 30px #00ff41; 
            }
        }

        /* Specific icon colors for each card */
        .email-icon { color: #ff6b6b; }
        .phone-icon { color: #4ecdc4; }
        .location-icon { color: #ffa726; }
        .about-icon { color: #ab47bc; }
        .facebook-icon { color: #1877f2; }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>
    <div class="code-bg" id="codeBg"></div>
    <div class="matrix-rain" id="matrixRain"></div>
    <div class="binary-bg" id="binaryBg"></div>
    
    <div class="floating-shapes">
        <i class="fas fa-code"></i>
        <i class="fas fa-laptop-code"></i>
        <i class="fas fa-terminal"></i>
        <i class="fas fa-database"></i>
    </div>

    <div class="container">
        <header class="header">
            <div class="profile-img">
                <img src="https://cdnjs.cloudflare.com/ajax/libs/twemoji/14.0.2/svg/1f9d1-1f4bb.svg" alt="Developer Avatar" onerror="this.style.display='none'; this.nextElementSibling.style.display='block';">
                <div class="profile-img-fallback">AP</div>
            </div>
            <h1 class="name glow-text">Aruna Pramodh</h1>
            <p class="subtitle">Welcome to my digital space</p>
            <a href="mailto:wickramanayakaarunapramodh@gmail.com" class="contact-btn">
                <i class="fas fa-envelope"></i> Get In Touch
            </a>
        </header>

        <div class="info-cards">
            <div class="card" style="animation-delay: 0.2s;">
                <i class="fas fa-envelope card-icon email-icon"></i>
                <h3>Email</h3>
                <p>wickramanayakaarunapramodh@gmail.com</p>
            </div>

            <div class="card" style="animation-delay: 0.4s;">
                <i class="fas fa-phone card-icon phone-icon"></i>
                <h3>Phone</h3>
                <p>+94722472939</p>
            </div>

            <div class="card" style="animation-delay: 0.6s;">
                <i class="fas fa-map-marker-alt card-icon location-icon"></i>
                <h3>Location</h3>
                <p>Galgamuwa, Sri Lanka</p>
            </div>

            <div class="card" style="animation-delay: 0.8s;">
                <a href="https://www.facebook.com/login/?next=https%3A%2F%2Fwww.facebook.com%2Fpramodhwicramanayaka" target="_blank" style="text-decoration: none; color: inherit;">
                    <i class="fab fa-facebook card-icon facebook-icon"></i>
                    <h3>Facebook</h3>
                    <p>Connect with me on Facebook</p>
                </a>
            </div>

            <div class="card" style="animation-delay: 1.0s;">
                <i class="fas fa-user-astronaut card-icon about-icon"></i>
                <h3>About Me</h3>
                <p>Passionate individual with a love for technology and innovation. Always eager to learn and explore new opportunities.</p>
            </div>
        </div>
    </div>

    <script>
        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 50;

            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                
                // Random size and position
                const size = Math.random() * 4 + 2;
                particle.style.width = size + 'px';
                particle.style.height = size + 'px';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                
                // Random animation delay and duration
                particle.style.animationDelay = Math.random() * 6 + 's';
                particle.style.animationDuration = (Math.random() * 3 + 3) + 's';
                
                particlesContainer.appendChild(particle);
            }
        }

        // Create programming code background
        function createCodeBackground() {
            const codeBg = document.getElementById('codeBg');
            const codeSnippets = [
                'const name = "Aruna Pramodh";',
                'function greeting() { return "Hello World!"; }',
                'if (coding === true) { console.log("Learning..."); }',
                'let skills = ["HTML", "CSS", "JavaScript"];',
                'for(let i = 0; i < dreams.length; i++) {',
                'class Developer { constructor(name) { this.name = name; } }',
                'async function fetchData() { const response = await api.get(); }',
                'const projects = { web: true, mobile: false };',
                'document.addEventListener("DOMContentLoaded", init);',
                'npm install success --save',
                'git commit -m "Added new features"',
                'SELECT * FROM opportunities WHERE location = "Sri Lanka";'
            ];

            function addCodeLine() {
                const codeLine = document.createElement('div');
                codeLine.className = 'code-line';
                codeLine.textContent = codeSnippets[Math.floor(Math.random() * codeSnippets.length)];
                codeLine.style.top = Math.random() * 100 + '%';
                codeLine.style.animationDuration = (Math.random() * 10 + 10) + 's';
                codeLine.style.animationDelay = Math.random() * 5 + 's';
                
                codeBg.appendChild(codeLine);

                setTimeout(() => {
                    if (codeLine.parentNode) {
                        codeLine.parentNode.removeChild(codeLine);
                    }
                }, 20000);
            }

            setInterval(addCodeLine, 2000);
        }

        // Create matrix rain effect
        function createMatrixRain() {
            const matrixContainer = document.getElementById('matrixRain');
            const matrixChars = '01アイウエオカキクケコサシスセソタチツテトナニヌネノハヒフヘホマミムメモヤユヨラリルレロワヲン';
            
            function createColumn() {
                const column = document.createElement('div');
                column.className = 'matrix-column';
                
                let text = '';
                const length = Math.random() * 20 + 10;
                for (let i = 0; i < length; i++) {
                    text += matrixChars[Math.floor(Math.random() * matrixChars.length)] + '<br>';
                }
                
                column.innerHTML = text;
                column.style.left = Math.random() * 100 + '%';
                column.style.animationDuration = (Math.random() * 3 + 2) + 's';
                column.style.animationDelay = Math.random() * 5 + 's';
                
                matrixContainer.appendChild(column);

                setTimeout(() => {
                    if (column.parentNode) {
                        column.parentNode.removeChild(column);
                    }
                }, 8000);
            }

            setInterval(createColumn, 500);
        }

        // Create binary background
        function createBinaryBackground() {
            const binaryBg = document.getElementById('binaryBg');
            
            for (let i = 0; i < 100; i++) {
                const digit = document.createElement('div');
                digit.className = 'binary-digit';
                digit.textContent = Math.random() > 0.5 ? '1' : '0';
                digit.style.left = Math.random() * 100 + '%';
                digit.style.top = Math.random() * 100 + '%';
                digit.style.animationDelay = Math.random() * 2 + 's';
                
                binaryBg.appendChild(digit);

                // Change digit randomly
                setInterval(() => {
                    digit.textContent = Math.random() > 0.5 ? '1' : '0';
                }, Math.random() * 3000 + 2000);
            }
        }

        // Mouse movement effect
        document.addEventListener('mousemove', (e) => {
            const cursor = document.createElement('div');
            cursor.style.position = 'fixed';
            cursor.style.left = e.clientX + 'px';
            cursor.style.top = e.clientY + 'px';
            cursor.style.width = '10px';
            cursor.style.height = '10px';
            cursor.style.background = 'rgba(0, 255, 65, 0.3)';
            cursor.style.borderRadius = '50%';
            cursor.style.pointerEvents = 'none';
            cursor.style.zIndex = '1000';
            cursor.style.animation = 'fadeOut 1s ease-out forwards';
            
            document.body.appendChild(cursor);
            
            setTimeout(() => {
                if (cursor.parentNode) {
                    cursor.parentNode.removeChild(cursor);
                }
            }, 1000);
        });

        // Add fadeOut animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes fadeOut {
                0% { opacity: 1; transform: scale(0); }
                50% { opacity: 1; transform: scale(1); }
                100% { opacity: 0; transform: scale(0); }
            }
        `;
        document.head.appendChild(style);

        // Card hover effects
        document.querySelectorAll('.card').forEach(card => {
            card.addEventListener('mouseenter', () => {
                card.style.background = 'rgba(255, 255, 255, 0.2)';
            });
            
            card.addEventListener('mouseleave', () => {
                card.style.background = 'rgba(255, 255, 255, 0.1)';
            });
        });

        // Smooth scroll effect for contact button
        document.querySelector('.contact-btn').addEventListener('click', (e) => {
            e.target.style.transform = 'scale(0.95)';
            setTimeout(() => {
                e.target.style.transform = 'translateY(-3px)';
            }, 150);
        });

        // Initialize all effects when page loads
        window.addEventListener('load', () => {
            createParticles();
            createCodeBackground();
            createMatrixRain();
            createBinaryBackground();
        });

        // Add typing effect to name
        const nameElement = document.querySelector('.name');
        const originalText = nameElement.textContent;
        nameElement.textContent = '';
        
        let i = 0;
        function typeWriter() {
            if (i < originalText.length) {
                nameElement.textContent += originalText.charAt(i);
                i++;
                setTimeout(typeWriter, 100);
            }
        }
        
        setTimeout(typeWriter, 1000);
    </script>

    <div class="card" style="animation-delay: 0.8s;">
                <a href="https://web.facebook.com/pramodwickramanayaka" target="_blank" style="text-decoration: none; color: inherit;">
                    <i class="fab fa-facebook card-icon facebook-icon"></i>
                    <h3>Facebook</h3>
                    <p>Connect with me on Facebook</p>
                </a>
            </div>

            <div class="card" style="animation-delay: 1.0s;">
                <a href="https://www.instagram.com/pramodwickramanayaka/" target="_blank" style="text-decoration: none; color: inherit;">
                    <i class="fab fa-instagram card-icon instagram-icon"></i>
                    <h3>Instagram</h3>
                    <p>Follow me on Instagram</p>
                </a>
            </div>

            <div class="card" style="animation-delay: 1.2s;">
                <a href="https://github.com/pramodwickramanayaka" target="_blank" style="text-decoration: none; color: inherit;">
                    <i class="fab fa-github card-icon github-icon"></i>
                    <h3>GitHub</h3>
                    <p>Check out my code projects</p>
                </a>
            </div>

            <div class="card" style="animation-delay: 1.4s;">
                <div style="cursor: pointer;" onclick="copyDiscordUsername()">
                    <i class="fab fa-discord card-icon discord-icon"></i>
                    <h3>Discord</h3>
                    <p>pramod_wickramanayaka<br><small>(Click to copy)</small></p>
                </div>
            </div>

            <div class="card" style="animation-delay: 1.6s;">
                <i class="fas fa-user-astronaut card-icon about-icon"></i>
                <h3>About Me</h3>
                <p>Passionate individual with a love for technology and innovation. Always eager to learn and explore new opportunities.</p>
            </div>
</body>
</html>
