---
title: Cookie Clicker
permalink: /cookieclicker/
layout: page
comments: true
---

# 🍪 Cookie Clicker

Welcome to the Cookie Clicker game! Click the cookie to collect cookies and buy bakers to increase your cookie production.

<div id="cookie" style="font-size: 100px; cursor: pointer;">🍪</div>
<audio id="clickSound" src="assets/ka-ching.mp3" preload="auto"></audio>

## Cookies: <span id="cookieCount">0</span>

## Bakers: <span id="bakerCount">0</span>

### Shop

You can buy bakers to increase your cookie production!

| Baker          | Cost | Increase Cookies Per Click | Action |
|----------------|------|----------------------------|--------|
| 👩‍🍳 Basic Baker  | 10   | +1                         | <button onclick="purchaseBaker(10, 1)">Purchase</button> |
| 👨‍🍳 Skilled Baker | 50   | +2                         | <button onclick="purchaseBaker(50, 2)">Purchase</button> |
| 👩‍🍳 Master Baker  | 100  | +5                         | <button onclick="purchaseBaker(100, 5)">Purchase</button> |

<script>
    let cookieCount = 0;
    let bakerCount = 0;
    let cookiesPerClick = 1;

    const cookieCountElement = document.getElementById("cookieCount");
    const bakerCountElement = document.getElementById("bakerCount");
    const cookieElement = document.getElementById("cookie");
    var clickSound = document.getElementById("clickSound");
    clickSound.playbackRate = 3;

    cookieElement.addEventListener("click", () => {
        clickSound.play();
        cookieCount += cookiesPerClick;
        cookieCountElement.innerText = cookieCount;
    });

    function purchaseBaker(cost, increase) {
        if (cookieCount >= cost) {
            cookieCount -= cost;
            bakerCount += 1;
            cookiesPerClick += increase;
            cookieCountElement.innerText = cookieCount;
            bakerCountElement.innerText = bakerCount;
        } else {
            alert("Not enough cookies!");
        }
    }
</script>
