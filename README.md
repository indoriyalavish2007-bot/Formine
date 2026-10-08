<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Something Special for You 💖</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }
        
        body {
            min-height: 100vh;
            min-height: 100dvh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 50%, #fbc2eb 100%);
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            overflow-x: hidden;
            position: relative;
            padding: 20px 16px;
        }
        
        .heart {
            position: absolute;
            font-size: 18px;
            animation: float 7s ease-in-out infinite;
            opacity: 0.5;
            pointer-events: none;
        }
        
        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            15% {
                opacity: 0.5;
            }
            85% {
                opacity: 0.5;
            }
            100% {
                transform: translateY(-80px) rotate(360deg);
                opacity: 0;
            }
        }
        
        .container {
            background: rgba(255, 255, 255, 0.96);
            padding: 36px 24px;
            border-radius: 24px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
            text-align: center;
            width: 100%;
            max-width: 380px;
            position: relative;
            z-index: 10;
            animation: popIn 0.7s ease;
        }
        
        @keyframes popIn {
            0% {
                transform: scale(0.85);
                opacity: 0;
            }
            100% {
                transform: scale(1);
                opacity: 1;
            }
        }
        
        .emoji {
            font-size: 52px;
            margin-bottom: 12px;
            animation: pulse 1.6s infinite;
        }
        
        @keyframes pulse {
            0%,
            100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.12);
            }
        }
        
        h1 {
            font-size: 24px;
            color: #e91e63;
            margin-bottom: 10px;
            font-weight: 700;
        }
        
        .message {
            font-size: 16px;
            color: #555;
            line-height: 1.55;
            margin-bottom: 18px;
        }
        
        .question {
            font-size: 22px;
            font-weight: 700;
            margin: 20px 0;
            background: linear-gradient(45deg, #f48fb1, #e91e63);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .btn-group {
            display: flex;
            gap: 12px;
            justify-content: center;
            margin-top: 26px;
            position: relative;
            min-height: 56px;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: 14px 28px;
            border: none;
            border-radius: 50px;
            font-size: 17px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.25s ease;
            box-shadow: 0 6px 16px rgba(0, 0, 0, 0.1);
            min-width: 120px;
            touch-action: manipulation;
        }
        
        .btn-yes {
            background: linear-gradient(45deg, #e91e63, #c2185b);
            color: white;
        }
        
        .btn-yes:active {
            transform: scale(0.96);
        }
        
        .btn-no {
            background: #f0f0f0;
            color: #666;
        }
        
        .btn-no:active {
            background: #e5e5e5;
        }
        
        .footer {
            margin-top: 26px;
            font-size: 13px;
            color: #999;
        }
        
        .success {
            display: none;
            margin-top: 18px;
            font-size: 18px;
            color: #e91e63;
            font-weight: 600;
            animation: popIn 0.4s ease;
            line-height: 1.4;
        }
        
        @media (max-width: 360px) {
            .container {
                padding: 28px 18px;
            }
            h1 {
                font-size: 22px;
            }
            .question {
                font-size: 20px;
            }
            .btn {
                padding: 13px 22px;
                font-size: 16px;
                min-width: 110px;
            }
        }
    </style>
</head>

<body>

    <!-- Audio player (hidden) -->
    <audio id="loveSong" preload="auto">
        <!-- Apna song yahan daal (Option 1) -->
        <source src="https://cs1.mp3.pm/download/205694078/N2h3VUNZK2kvSUZJSmJqek16eHhNeTJYdGlSTW5Yd3FGb05TQ0RaT1MvNFBLVXlzNEszdFIxZEJxSzN0cEpEY3FJOEh1SmtGb2dsWkdCb29HNHlQd2N4VFZsdE1sWExWVlVJbWZDNmxCaXpPZ2JaRGQybG9BcDVsZjY2aUx5cE0/Edd_Sheeran_-_Perfect_(mp3.pm).mp3" type="audio/mpeg">
        
    </audio>

    <div class="heart" style="left: 8%; animation-delay: 0s;">💖</div>
    <div class="heart" style="left: 22%; animation-delay: 1.2s;">💕</div>
    <div class="heart" style="left: 68%; animation-delay: 2.4s;">💗</div>
    <div class="heart" style="left: 82%; animation-delay: 3.5s;">💘</div>
    <div class="heart" style="left: 40%; animation-delay: 4.8s;">❤️</div>
    <div class="heart" style="left: 55%; animation-delay: 6s;">💞</div>

    <div class="container">
        <div class="emoji">💖</div>

        <h1>Hey Anjuu...</h1>

        <div class="message">
            I have made something special for you…
        </div>

        <div class="question">
            Will you be mine??
        </div>

        <div class="message">
            A little reminder of how special you are to me.<br> Open this with love 💕
        </div>

        <div class="btn-group">
            <button class="btn btn-yes" onclick="sayYes()">Yes 💕</button>
            <button class="btn btn-no" onclick="sayNo()">No</button>
        </div>

        <div class="success" id="successMsg">
            Yesss! I Love You Too Much!! Mine Kuchu Puchu🥹💖
        </div>

        <div class="footer">
            Made with pure feelings 💌
        </div>
    </div>

    <script>
        function sayYes() {
            // No button hide
            const noBtn = document.querySelector('.btn-no');
            if (noBtn) {
                noBtn.style.display = 'none';
            }

            // Success message
            document.getElementById('successMsg').style.display = 'block';

            // Yes button change
            const yesBtn = document.querySelector('.btn-yes');
            yesBtn.innerHTML = "She said Yes 💕";
            yesBtn.style.pointerEvents = 'none';
            yesBtn.style.opacity = '0.9';

            // Song play
            const song = document.getElementById('loveSong');
            song.currentTime = 0;
            song.play().catch(function(error) {
                console.log("Song play nahi hua:", error);
            });
        }

        function sayNo() {
            const noBtn = document.querySelector('.btn-no');
            noBtn.style.position = 'absolute';
            noBtn.style.left = Math.random() * 55 + '%';
            noBtn.style.top = Math.random() * 50 + 20 + '%';
            noBtn.style.zIndex = '20';
            alert("Please Dont Say No😫😫");
        }
    </script>
</body>

</html>
