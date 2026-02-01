<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Valentine 💖</title>

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">

<style>
    body {
        margin: 0;
        height: 100vh;
        background: pink;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: 'Pacifico', cursive;
    }

    .container {
        text-align: center;
    }

    h1 {
        font-size: 3rem;
        color: #b3005e;
        margin-bottom: 40px;
    }

    button {
        font-size: 1.5rem;
        padding: 10px 25px;
        border: none;
        border-radius: 10px;
        cursor: pointer;
        margin: 10px;
        position: relative;
    }

    #yes {
        background: #ff4d88;
        color: white;
    }

    #no {
        background: #444;
        color: white;
        position: absolute;
    }

    #imageBox {
        display: none;
        margin-top: 30px;
    }

    img {
        max-width: 300px;
        border-radius: 20px;
        box-shadow: 0 0 20px rgba(0,0,0,0.3);
    }
</style>
</head>

<body>
<div class="container">
    <h1>Niharika will you be my Valentine?</h1>

    <button id="yes" onclick="showImage()">Yes 💖</button>
    <button id="no" onmouseover="moveNo()">No 💔</button>

    <div id="imageBox">
        <img src="valentine.jpg" alt="Valentine Image">
    </div>
</div>

<script>
    function moveNo() {
        const noBtn = document.getElementById("no");
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 100);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    }

    function showImage() {
        document.getElementById("imageBox").style.display = "block";
    }
</script>
</body>
</html>
