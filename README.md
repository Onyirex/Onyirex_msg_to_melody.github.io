<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Melody ✨</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@400;600&display=swap');
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: #0f0c29;
            background: linear-gradient(to right, #0f0c29, #302b63, #24243e);
            color: white;
            text-align: center;
            padding: 20px;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 40px 20px;
            opacity: 0;
            animation: fadeIn 2s forwards 0.5s;
        }
        
        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: #ff6b6b;
            text-shadow: 0 0 10px rgba(255, 107, 107, 0.5);
        }
        
        p {
            font-size: 1.2rem;
            margin: 25px 0;
            opacity: 0;
            animation: slideUp 1s forwards;
        }
        
        p:nth-child(2) { animation-delay: 1s; }
        p:nth-child(3) { animation-delay: 1.5s; }
        p:nth-child(4) { animation-delay: 2s; }
        p:nth-child(5) { animation-delay: 2.5s; }
        p:nth-child(6) { animation-delay: 3s; }
        p:nth-child(7) { animation-delay: 3.5s; }
        p:nth-child(8) { animation-delay: 4s; }
        p:nth-child(9) { animation-delay: 4.5s; }
        p:nth-child(10) { animation-delay: 5s; }
        
        .signature {
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            margin-top: 40px;
            color: #ff6b6b;
        }
        
        .hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .heart {
            position: absolute;
            font-size: 20px;
            opacity: 0;
            animation: float 6s ease-in infinite;
        }
        
        @keyframes fadeIn {
            to { opacity: 1; }
        }
        
        @keyframes slideUp {
            from { transform: translateY(20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
        }
        
        .emoji {
            font-size: 1.5rem;
            vertical-align: middle;
        }
    </style>
</head>
<body>
    <div class="hearts" id="hearts"></div>
    
    <div class="container">
        <h1>For Melody ✨</h1>
        
        <p>From the moment I met you, the day the universe decided to gift the world with you—I knew I was in trouble.</p>
        
        <p>I knew that I would simp like a complete idiot. I knew that I'd be obsessed.</p>
        
        <p>But I’ll own it proudly and would shout from the rooftops ~ <em>*I'm Melody's biggest fan*</em> <span class="emoji">🔥</span></p>
        
        <p>Girl...</p>
        
        <p><span class="emoji">✨️</span> You’re pure magic — the kind that turns ordinary moments into memories I replay like my favorite song.</p>
        
        <p><span class="emoji">✨</span> You’re the chorus I can’t get out of my head.</p>
        
        <p><span class="emoji">✨</span> The harmony that makes my heart feel whole.</p>
        
        <p><span class="emoji">✨</span> And the only person I'd happily lose sleep over just to hear you laugh.</p>
        
        <p>Today, I wish I could spoil you silly — cake for breakfast, dancing ‘til 3 a.m., and a party as bright as your smile.</p>
        
        <p>For now, just know:<br>You’re loved wildly, missed deeply, and celebrated more than words can hold.</p>
        
        <p>May lines continue to fall in pleasant places for you.<br>Stay beautiful, strong, happy and awesome. <span class="emoji">🤗💫</span></p>
        
        <p class="signature">Cheers <span class="emoji">🥂</span></p>
    </div>
    
    <script>
        // Floating hearts animation
        const heartsContainer = document.getElementById('hearts');
        const emojis = ['❤️', '🧡', '💛', '💚', '💙', '💜', '🤎', '🖤', '🤍'];
        
        function createHeart() {
            const heart = document.createElement('div');
            heart.className = 'heart';
            heart.innerHTML = emojis[Math.floor(Math.random() * emojis.length)];
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 3 + 3 + 's';
            heartsContainer.appendChild(heart);
            
            setTimeout(() => {
                heart.remove();
            }, 6000);
        }
        
        setInterval(createHeart, 300);
    </script>
</body>
</html>
