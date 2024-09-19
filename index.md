---
layout: base
title: Student Home
description: Home Page
hide: true
---
<p style="text-align: center; font-size: 40px; color: #89CFF0;"> Jacob's pro coding page 
</p>
<br>
<br>

# Cookie Clicker Game

<style>
    body {
        font-family: Arial, sans-serif;
        background-color: #f0f0f0;
        text-align: center;
    }
    #cookieImage {
        width: 150px; /* Adjust size as needed */
        cursor: pointer;
    }
    button {
        padding: 10px 15px;
        font-size: 16px;
        margin: 5px;
        cursor: pointer;
    }
    #upgradeSection, #achievementSection {
        margin-top: 20px;
        padding: 10px;
        background-color: #fff;
        border: 1px solid #ccc;
    }
</style>

<img id="cookieImage" src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/Cookie_icon.svg/2048px-Cookie_icon.svg.png" alt="Cookie" />
<p>Cookies: <span id="cookieCount">0</span></p>
<p>Cookies per Second: <span id="cookiesPerSecond">0</span></p>

<div id="upgradeSection">
    <h3>Upgrades</h3>
    <button id="upgradeButton">Buy Upgrade (Cost: 10 cookies)</button>
    <button id="autoClickerButton">Buy Auto-Clicker (Cost: 50 cookies)</button>
    <button id="doubleClickButton">Buy Double Click Upgrade (Cost: 100 cookies)</button>
</div>

<div id="achievementSection">
    <h3>Achievements</h3>
    <ul id="achievementList"></ul>
</div>

<audio controls src="707db471-c834-494e-a3d9-ada985203ef6.mp3" title="Title"></audio>

<script>
    let cookies = 0;
    let cookiesPerClick = 1;
    let cookiesPerSecond = 0;
    let autoClickerCount = 0;
    let achievements = [];

    // Update the cookie count display
    function updateDisplay() {
        document.getElementById('cookieCount').innerText = cookies;
        document.getElementById('cookiesPerSecond').innerText = cookiesPerSecond;
    }

    // Play sound effect
    function playSound() {
        const sound = document.getElementById('clickSound');
        sound.currentTime = 0; // Restart sound if it's playing
        sound.play();
    }

    // Handle cookie click
    document.getElementById('cookieImage').addEventListener('click', () => {
        cookies += cookiesPerClick;
        playSound(); // Play sound on click
        checkAchievements();
        updateDisplay();
    });

    // Check for achievements
    function checkAchievements() {
        if (cookies === 100 && !achievements.includes("100 Cookies")) {
            achievements.push("100 Cookies");
            addAchievement("100 Cookies!");
        }
        if (cookies === 1000 && !achievements.includes("1000 Cookies")) {
            achievements.push("1000 Cookies");
            addAchievement("1000 Cookies!");
        }
    }

    function addAchievement(achievement) {
        const li = document.createElement("li");
        li.innerText = achievement;
        document.getElementById('achievementList').appendChild(li);
    }

    // Handle upgrade purchase
    document.getElementById('upgradeButton').addEventListener('click', () => {
        if (cookies >= 10) {
            cookies -= 10;
            cookiesPerClick++;
            alert('Upgrade purchased! Cookies per click: ' + cookiesPerClick);
            updateDisplay();
        } else {
            alert('Not enough cookies!');
        }
    });

    // Handle auto-clicker purchase
    document.getElementById('autoClickerButton').addEventListener('click', () => {
        if (cookies >= 50) {
            cookies -= 50;
            autoClickerCount++;
            cookiesPerSecond += 1; // Each auto-clicker adds 1 cookie per second
            alert('Auto-Clicker purchased! Total auto-clickers: ' + autoClickerCount);
            updateDisplay();
        } else {
            alert('Not enough cookies!');
        }
    });

    // Handle double click upgrade
    document.getElementById('doubleClickButton').addEventListener('click', () => {
        if (cookies >= 100) {
            cookies -= 100;
            cookiesPerClick *= 2; // Double the cookies per click
            alert('Double Click Upgrade purchased! Cookies per click: ' + cookiesPerClick);
            updateDisplay();
        } else {
            alert('Not enough cookies!');
        }
    });

    // Generate cookies automatically
    setInterval(() => {
        cookies += cookiesPerSecond;
        updateDisplay();
    }, 1000);
</script>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Snake Game Launcher</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
        }
        button {
            padding: 10px 15px;
            font-size: 16px;
            cursor: pointer;
            margin: 20px;
        }
    </style>
</head>
<body>

<h1>The Better Snake Game</h1>
<button id="launchButton">Click Me</button>

<script>
    document.getElementById('launchButton').addEventListener('click', function() {
        window.open('snake_game.html', 'Snake Game', 'width=450,height=500');
    });
</script>

</body>
</html>

 

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

