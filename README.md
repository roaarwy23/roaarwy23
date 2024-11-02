<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Professional 3D Heart - SIMA</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }
        body {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #e0e0e0, #f7f7f7);
            color: #333;
        }
        .heart-container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .heart {
            position: relative;
            width: 120px;
            height: 120px;
            background: linear-gradient(135deg, #ff4d4d, #ff1a1a);
            transform: rotate(-45deg);
            animation: pulse 2s infinite, gradientShift 5s infinite;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        .heart::before, .heart::after {
            content: "";
            position: absolute;
            width: 120px;
            height: 120px;
            background: inherit;
            border-radius: 50%;
        }
        .heart::before {
            top: -60px;
            left: 0;
        }
        .heart::after {
            left: 60px;
            top: 0;
        }
        .heart-name {
            margin-top: 20px;
            font-size: 1.5rem;
            color: #ff1a1a;
            letter-spacing: 2px;
            animation: fadeIn 2s ease-in-out;
        }
        footer {
            position: absolute;
            bottom: 10px;
            font-size: 0.9rem;
            color: #777;
            letter-spacing: 1px;
        }
        @keyframes pulse {
            0%, 100% {
                transform: scale(1) rotate(-45deg);
            }
            50% {
                transform: scale(1.1) rotate(-45deg);
            }
        }
        @keyframes gradientShift {
            0% {
                background: linear-gradient(135deg, #ff4d4d, #ff1a1a);
            }
            50% {
                background: linear-gradient(135deg, #ff8080, #ff4040);
            }
            100% {
                background: linear-gradient(135deg, #ff4d4d, #ff1a1a);
            }
        }
        @keyframes fadeIn {
            0% {
                opacity: 0;
                transform: translateY(20px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }
        /* Hover effect for heart */
        .heart:hover {
            transform: scale(1.2) rotate(-45deg);
            transition: transform 0.3s ease-in-out;
        }
    </style>
</head>
<body>
    <div class="heart-container">
        <div class="heart"></div>
        <div class="heart-name">SIMA</div>
    </div>
    <footer>© سيما الغبيه .</footer>
</body>
</html>
