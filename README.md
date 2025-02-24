<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Love Website</title>
    <style>
        body {
            text-align: center;
            background-color: #ffcccb;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
        }
        h1 {
            color: #d63384;
            margin-top: 50px;
        }
        button {
            background-color: #ff4081;
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 10px;
            margin-top: 20px;
        }
        button:hover {
            background-color: #d81b60;
        }
        .message {
            font-size: 24px;
            color: #d63384;
            display: none;
            margin-top: 20px;
        }
        .heart {
            position: absolute;
            color: red;
            font-size: 20px;
            animation: float 5s infinite;
        }
        @keyframes float {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            50% { transform: translateY(-300px) scale(1.5); opacity: 0.6; }
            100% { transform: translateY(-600px) scale(2); opacity: 0; }
        }
    </style>
</head>
<body>
    <h1>Chào em yêu! ❤️</h1>
    <button onclick="showMessage()">Nhấn vào đây</button>
    <p class="message">Anh yêu em nhiều lắm! 💖💖💖</p>
    
    <script>
        function showMessage() {
            document.querySelector('.message').style.display = 'block';
        }
        function createHeart() {
            let heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '❤️';
            document.body.appendChild(heart);
            
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.top = '100vh';
            heart.style.animationDuration = (Math.random() * 3 + 2) + 's';
            
            setTimeout(() => { heart.remove(); }, 5000);
        }
        setInterval(createHeart, 500);
    </script>
</body>
</html>
