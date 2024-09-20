---
layout: base
title: The Nighty Nighthawk Page of Jacob
description: Home Page
hide: true
---
<p style="text-align: center; font-size: 40px; color: #89CFF0;"> Jacob's pro coding page 
</p>
<br>
<br>




<p style="text-align: center;">
    <img src="image.png" alt="Image Description" style="width: 45%; margin-right: 10px; display: inline-block;">
    <img src="image-1.png" alt="Image Description" style="width: 45%; display: inline-block;">
</p>

<p style="text-align: center; font-size: 25px;"> Proud 49ers and Warriors fan
<br>
<br>
<p style="text-align: center; font-size: 25px;"> The two best foods
<p style="text-align: center;">
    <img src="image-4.png" alt="Image Description" style="width: 45%; hieght: 45%; margin-right: 10px; display: inline-block;">
    <img src="image-5.png" alt="Image Description" style="width: 45%; display: inline-block;">
</p>
<p style="text-align: center; font-size: 15px;"> If you somehow don't like these foods that is a problem. They are simply just the best and most accesable foods. Tacos you can find anywhere in different viraties. Chicken alfredo no matter where you get it from it has a consistant taste and is always a good option.
<div style="text-align: center;">
    <button style="
        display: inline-block;
        padding: 10px 20px;
        font-size: 16px;
        font-weight: bold;
        text-decoration: none;
        color: white;
        background-color: #007bff;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.3s, transform 0.2s;
    ">I don't do anything!</button>
</div>
<div style="text-align: center;">
    <a href="https://google.com" style="
        display: inline-block;
        padding: 10px 20px;
        font-size: 16px;
        font-weight: bold;
        text-decoration: none;
        color: white;
        background-color: #007bff;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.3s, transform 0.2s;
    ">Google</a>
    <a href="https://www.youtube.com/watch?v=0a5hUOTn8xA&t=36s" style="
        display: inline-block;
        padding: 10px 20px;
        font-size: 16px;
        font-weight: bold;
        text-decoration: none;
        color: white;
        background-color: #FFD700;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.3s, transform 0.2s;
    ">Goat</a>
</div>
<br>
<br>
<br>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DON'T PRESS ME</title>
    <style>
        body {
            font-family: Arial, sa ns-serif;
            text-align: center;
            margin-top: 50px;
            background-color: #f0f0f0;
        }
        button {
            padding: 15px 30px;
            font-size: 20px;
            cursor: pointer;
            background-color: #bb86fc;
            color: white;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #3700b3;
        }
    </style>
</head>
<body>
    <h1>U Should Press Me</h1>
    <button id="soundButton">Play Sound</button>
    <audio id="sound" src="Stupid.mp3" preload="auto"></audio>

    <script>
        let isPlaying = false;

        document.getElementById('soundButton').addEventListener('click', () => {
            if (!isPlaying) {
                isPlaying = true;
                playSound();
            }
        });

        function playSound() {
            const sound = document.getElementById('sound');
            sound.currentTime = 0; // Restart sound
            sound.play().catch(error => {
                console.error("Error playing sound:", error);
            });
            sound.addEventListener('ended', playSound); // Play again when sound ends
        }
    </script>
</body>
</html>
