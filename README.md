<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Do You Love Me?</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #ffd1dc;
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
        }
        .container {
            background: white;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            width: 90%;
        }
        img {
            max-width: 100%;
            border-radius: 10px;
        }
        h1 {
            color: #ff4d6d;
            margin: 20px 0;
        }
        .buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: 0.3s;
        }
        .yes-btn {
            background-color: #ff4d6d;
            color: white;
        }
        .no-btn {
            background-color: #8d99ae;
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNHJueGZ4bm40bm5ueGZ4bm40bm5ueGZ4bm40bm5ueGZ4bm40JmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/3o7TKMGpxxHOGTdzJC/giphy.gif" alt="Cute Cartoon">
        <h1>Do you love me?</h1>
        <div class="buttons">
            <button class="yes-btn" onclick="nextPage()">Yes!</button>
            <button class="no-btn" id="noButton" onmouseover="moveButton()">No</button>
        </div>
    </div>

    <script>
        function nextPage() {
            window.location.href = "yes.html";
        }

        function moveButton() {
            const noButton = document.getElementById("noButton");
            const x = Math.random() * (window.innerWidth - noButton.offsetWidth);
            const y = Math.random() * (window.innerHeight - noButton.offsetHeight);
            noButton.style.position = "absolute";
            noButton.style.left = x + "px";
            noButton.style.top = y + "px";
        }
    </script>
</body>
</html>
