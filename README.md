# Valentine-website


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: pink;
            margin: 0;
            padding: 0;
        }
        h1 {
            margin-top: 50px;
        }
        #cat-image {
            width: 200px;
            height: auto;
            transition: transform 0.3s;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .yes-btn {
            background-color: red;
            color: white;
        }
        .no-btn {
            background-color: white;
            color: black;
            border: 1px solid black;
            position: absolute;
        }
    </style>
</head>
<body>

    <h1>Will you be my valentine, baby girl? ❤️</h1>
    <img id="cat-image" src="https://i.imgur.com/OiP4wOD.png" alt="Happy Cat">
    
    <div class="buttons">
        <button class="yes-btn" onclick="showHappy()">Yes</button>
        <button class="no-btn" onclick="showSad()" id="noButton">No</button>
    </div>

    <audio id="bg-music" autoplay loop>
        <source src="https://example.com/lovers.mp3" type="audio/mp3">
    </audio>

    <script>
        let noButton = document.getElementById("noButton");

        function showHappy() {
            document.getElementById("cat-image").src = "https://i.imgur.com/OiP4wOD.png"; // Happy Cat Image
            alert("Yay! I love you baby girl! ❤️");
        }

        function showSad() {
            document.getElementById("cat-image").src = "https://i.imgur.com/3T1QfMl.png"; // Sad Cat Image
            moveNoButton();
        }

        function moveNoButton() {
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            noButton.style.left = `${x}px`;
            noButton.style.top = `${y}px`;
        }
    </script>

</body>
</html>
