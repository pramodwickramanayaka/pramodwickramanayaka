<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0">
    
    <title>Aruna Pramod | Official Portfolio</title>
	<link rel="icon" type="image/png" href="1770829522007.jpg">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap');

        body, html {
            margin: 0;
            padding: 0;
            font-family: 'Inter', sans-serif;
            background-color: #000000;
            color: #ffffff;
            display: flex;
            justify-content: center;
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* Entrance Animations */
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .reveal { opacity: 0; animation: fadeInUp 0.8s ease forwards; }
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }
        .delay-4 { animation-delay: 0.8s; }
        .delay-5 { animation-delay: 0.9s; }
        .delay-6 { animation-delay: 1.0s; }
        .delay-7 { animation-delay: 1.1s; }

        .page-full-wrap {
            width: 100%;
            max-width: 580px;
            padding: 50px 24px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .profile-img {
            width: 115px;
            height: 115px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 18px;
            border: 2px solid #1a1a1a;
        }

        .name-container {
            display: flex;
            align-items: center;
            gap: 6px;
            margin-bottom: 12px;
        }

        h1 {
            font-size: 22px;
            font-weight: 800;
            margin: 0;
            letter-spacing: 1.5px;
            text-transform: uppercase;
        }

        .bio-container {
            text-align: center;
            margin-bottom: 5px;
            max-width: 90%;
        }

        .bio-quote {
            font-size: 15px;
            color: #ffffff;
            font-weight: 500;
            display: block;
            margin-bottom: 10px;
            line-height: 1.4;
            opacity: 0.8;
        }

        /* Typewriter Styling */
        .typewriter-box {
            height: 20px;
            margin-bottom: 40px;
        }

        .typewriter-text {
            font-size: 14px;
            color: #0095f6;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            border-right: 2px solid #0095f6;
            padding-right: 5px;
            animation: blink 0.7s infinite;
        }

        @keyframes blink { 50% { border-color: transparent; } }

        .links-container {
            width: 100%;
            display: flex;
            flex-direction: column;
            gap: 18px;
        }

        .link-each {
            width: 100%;
            height: 65px;
            background-color: #111111;
            border: 1.5px solid #222222;
            border-radius: 14px;
            text-decoration: none;
            color: #ffffff;
            font-size: 17px;
            font-weight: 600;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            transition: all 0.25s ease;
        }

        .link-each:hover {
            transform: scale(1.02);
            background-color: #1a1a1a;
            border-color: #0095f6;
        }

        .link-each i, .link-each svg {
            position: absolute;
            left: 25px;
            font-size: 22px;
        }

        footer {
            margin-top: 80px;
            text-align: center;
            width: 100%;
        }

        .footer-brand {
            font-size: 18px;
            font-weight: 800;
            letter-spacing: 5px;
            color: #ffffff;
            margin-bottom: 5px;
        }

        .footer-sub {
            font-size: 11px;
            color: #555;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 20px;
        }

        .copyright {
            font-size: 12px;
            color: #333;
            border-top: 1px solid #111;
            padding-top: 20px;
        }
    </style>
</head>
<body>

    <div class="page-full-wrap">
        <div class="reveal delay-1">
            <a href="https://web.facebook.com/pramodwickramanayaka" target="_blank">
                <img src="1770829522007.jpg" alt="Aruna Pramod" class="profile-img">
            </a>
        </div>
        
        <div class="name-container reveal delay-2">
            <h1>ARUNA PRAMOD</h1>
            <svg width="22" height="22" viewBox="0 0 24 24" fill="#0095f6">
                <path d="M22.5 12.5c0-1.58-.88-2.95-2.18-3.66.15-.44.23-.91.23-1.4 0-2.45-1.99-4.44-4.44-4.44-.49 0-.96.08-1.4.23-1.17-1.3-2.35-2.23-3.66-2.23s-2.49.93-3.66 2.23c-.44-.15-.91-.23-1.4-.23-2.45 0-4.44 1.99-4.44 4.44 0 .49.08.96.23 1.4-1.3.71-2.18 2.08-2.18 3.66 0 1.58.88 2.95 2.18 3.66-.15.44-.23.91-.23 1.4 0 2.45 1.99 4.44 4.44 4.44.49 0 .96-.08 1.4-.23 1.17 1.3 2.35 2.23 3.66 2.23s2.49-.93 3.66-2.23c.44.15.91.23 1.4.23 2.45 0 4.44-1.99 4.44-4.44 0-.49-.08-.96-.23-1.4 1.3-.71 2.18-2.08 2.18-3.66zm-12.7 4.1l-3.3-3.3 1.4-1.4 1.9 1.9 4.9-4.9 1.4 1.4-6.3 6.3z"></path>
            </svg>
        </div>
        
        <div class="bio-container reveal delay-3">
            <span class="bio-quote">"Focus on Gaming, not Girls. Because Emotions are temporary, but Gaming is permanent"</span>
        </div>

        <div class="typewriter-box reveal delay-4">
            <span class="typewriter-text" id="typewriter"></span>
        </div>

        <div class="links-container">
            <a href="https://www.tiktok.com/@pramodwickramanayaka" target="_blank" class="link-each reveal delay-4">
                <i class="fab fa-tiktok"></i> TikTok
            </a>
            <a href="https://www.instagram.com/pramodwickramanayaka/#" target="_blank" class="link-each reveal delay-5">
                <i class="fab fa-instagram"></i> Instagram
            </a>
            <a href="https://web.facebook.com/pramodwickramanayaka" target="_blank" class="link-each reveal delay-6">
                <i class="fab fa-facebook-f"></i> Facebook
            </a>
            <a href="https://x.com/Rebornpramod" target="_blank" class="link-each reveal delay-7">
                <svg width="20" height="20" fill="white" viewBox="0 0 24 24"><path d="M18.901 1.153h3.68l-8.04 9.19L24 22.846h-7.406l-5.8-7.584-6.638 7.584H.474l8.6-9.83L0 1.154h7.594l5.243 6.932 6.064-6.932zm-1.294 19.486h2.039L6.486 3.24H4.298l13.309 17.398z"/></svg>
                X (Twitter)
            </a>
        </div>

        <footer class="reveal delay-7">
            <div class="footer-brand">DRS EDITS</div>
            <div class="footer-sub">Official Portfolio • Visual Arts • Gaming</div>
            <div class="copyright">© 2026 <b>ARUNA PRAMOD</b>. ALL RIGHTS RESERVED.</div>
        </footer>
    </div>

    <script>
        const textElement = document.getElementById('typewriter');
        const phrases = ["Rising Video Editor", "Visual Storyteller", "GTA V Online Player", "Spotify Lover"];
        let pIdx = 0, cIdx = 0, isDel = false, speed = 100;

        function type() {
            const current = phrases[pIdx];
            textElement.textContent = isDel ? current.substring(0, cIdx--) : current.substring(0, cIdx++);
            speed = isDel ? 50 : 100;

            if (!isDel && cIdx > current.length) { isDel = true; speed = 2000; }
            else if (isDel && cIdx < 0) { isDel = false; pIdx = (pIdx + 1) % phrases.length; speed = 500; }
            setTimeout(type, speed);
        }
        document.addEventListener('DOMContentLoaded', type);
    </script>
</body>
</html>

