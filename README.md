<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AIアシスタント</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        .container {
            text-align: center;
            padding: 40px;
        }
        
        .ai-visual {
            position: relative;
            width: 300px;
            height: 300px;
            margin: 0 auto 30px;
        }
        
        .circle {
            position: absolute;
            border-radius: 50%;
            animation: pulse 3s ease-in-out infinite;
        }
        
        .circle1 {
            width: 300px;
            height: 300px;
            background: rgba(255, 255, 255, 0.1);
            top: 0;
            left: 0;
            animation-delay: 0s;
        }
        
        .circle2 {
            width: 240px;
            height: 240px;
            background: rgba(255, 255, 255, 0.15);
            top: 30px;
            left: 30px;
            animation-delay: 0.5s;
        }
        
        .circle3 {
            width: 180px;
            height: 180px;
            background: rgba(255, 255, 255, 0.2);
            top: 60px;
            left: 60px;
            animation-delay: 1s;
        }
        
        .core {
            position: absolute;
            width: 120px;
            height: 120px;
            background: linear-gradient(135deg, #ffffff 0%, #f0f0f0 100%);
            border-radius: 50%;
            top: 90px;
            left: 90px;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
            animation: float 4s ease-in-out infinite;
        }
        
        .core::before {
            content: '';
            position: absolute;
            width: 40px;
            height: 40px;
            background: #667eea;
            border-radius: 50%;
            animation: glow 2s ease-in-out infinite;
        }
        
        .particles {
            position: absolute;
            width: 100%;
            height: 100%;
        }
        
        .particle {
            position: absolute;
            width: 6px;
            height: 6px;
            background: white;
            border-radius: 50%;
            animation: orbit 8s linear infinite;
        }
        
        .particle:nth-child(1) {
            top: 20px;
            left: 150px;
            animation-delay: 0s;
        }
        
        .particle:nth-child(2) {
            top: 80px;
            left: 280px;
            animation-delay: 2s;
        }
        
        .particle:nth-child(3) {
            top: 220px;
            left: 260px;
            animation-delay: 4s;
        }
        
        .particle:nth-child(4) {
            top: 260px;
            left: 100px;
            animation-delay: 6s;
        }
        
        .particle:nth-child(5) {
            top: 140px;
            left: 10px;
            animation-delay: 1s;
        }
        
        h1 {
            color: white;
            font-size: 2.5em;
            margin: 0 0 15px 0;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
        }
        
        p {
            color: rgba(255, 255, 255, 0.9);
            font-size: 1.2em;
            margin: 0;
            text-shadow: 0 1px 5px rgba(0, 0, 0, 0.2);
        }
        
        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
                opacity: 0.6;
            }
            50% {
                transform: scale(1.05);
                opacity: 0.8;
            }
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-15px);
            }
        }
        
        @keyframes glow {
            0%, 100% {
                box-shadow: 0 0 20px rgba(102, 126, 234, 0.5);
            }
            50% {
                box-shadow: 0 0 40px rgba(102, 126, 234, 0.8);
            }
        }
        
        @keyframes orbit {
            from {
                transform: rotate(0deg) translateX(140px) rotate(0deg);
            }
            to {
                transform: rotate(360deg) translateX(140px) rotate(-360deg);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="ai-visual">
            <div class="circle circle1"></div>
            <div class="circle circle2"></div>
            <div class="circle circle3"></div>
            <div class="core"></div>
            <div class="particles">
                <div class="particle"></div>
                <div class="particle"></div>
                <div class="particle"></div>
                <div class="particle"></div>
                <div class="particle"></div>
            </div>
        </div>
        <h1>AIアシスタント</h1>
        <p>いつでもお手伝いします</p>
    </div>
</body>
</html>
