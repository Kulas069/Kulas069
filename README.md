<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Proposal</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(to right, #ff758c, #ff7eb3);
            text-align: center;
            font-family: 'Arial', sans-serif;
        }
        .container {
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            max-width: 400px;
        }
        h1 {
            color: #d63384;
        }
        .buttons {
            margin-top: 20px;
        }
        .buttons button {
            margin: 10px;
            padding: 12px 25px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            transition: 0.3s;
        }
        .yes {
            background-color: #28a745;
            color: white;
        }
        .yes:hover {
            background-color: #218838;
        }
        .no {
            background-color: #6c757d;
            color: white;
            position: absolute;
        }
        #message {
            font-size: 18px;
            font-weight: bold;
            color: #d63384;
            margin-top: 15px;
        }
    </style>
    <script>
        function moveNoButton() {
            let btn = document.getElementById('noBtn');
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 100);
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }
        function showMessage() {
            document.getElementById('message').innerHTML = "Thanks, boss! I'll send a poem if you see this na ❤️";
        }
    </script>
</head>
<body>
    <div class="container">
        <h1>Will You Be My Valentine? 💖</h1>
        <div class="buttons">
            <button class="yes" onclick="showMessage()">Yes!</button>
            <button class="no" id="noBtn" onmouseover="moveNoButton()">No</button>
        </div>
        <p id="message"></p>
    </div>
</body>
</html>
