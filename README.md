<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Holi!</title>
    <style>
        body {
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }
        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.4);
            z-index: 100;
            animation: fadeIn 0.5s ease-in-out;
        }
        .btn {
            padding: 10px 20px;
            background: #ff4081;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            transition: background 0.3s;
        }
        .btn:hover {
            background: #d81b60;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translate(-50%, -55%); }
            to { opacity: 1; transform: translate(-50%, -50%); }
        }
        .color-splash {
            position: absolute;
            width: 100px;
            height: 100px;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 30%, rgba(0,0,0,0) 80%);
            border-radius: 50%;
            opacity: 0.8;
            animation: splashAnimation 1s ease-out forwards;
        }
        @keyframes splashAnimation {
            from { transform: scale(0); opacity: 1; }
            to { transform: scale(3); opacity: 0; }
        }
    </style>
</head>
<body>
    <div class="popup" id="popup">
        <h2>🎨 Happy Holi, Shakshi! 🎉</h2>
        <p>May your life be filled with colors of joy and happiness! 🌸✨</p>
        <button class="btn" onclick="closePopup()">Enjoy!</button>
    </div>
    <script>
        window.onload = function() {
            document.getElementById("popup").style.display = "block";
            createColorSplashes();
        };

        function closePopup() {
            document.getElementById("popup").style.display = "none";
        }

        function createColorSplashes() {
            let colors = ['#FF5733', '#FFBD33', '#33FF57', '#335BFF', '#DA33FF'];
