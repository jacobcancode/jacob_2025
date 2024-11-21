---
layout: page
title: Profile Work
permalink: /profilework/
comments: false
---

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profile Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
        }
        .profile-container {
            background: light grey;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            margin: auto;
            text-align: center;
        }
        .profile-icon {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
            cursor: pointer;
            border: 2px solid #ddd;
            margin-bottom: 15px;
        }
        .input-field {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
        }
        input[type="text"],
        input[type="file"] {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        button {
            padding: 10px 15px;
            background-color: #5cb85c;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #4cae4c;
        }
    </style>
</head>
<body>

<div class="profile-container">
    <h2>Profile</h2>
    <img id="profileIcon" class="profile-icon" src="default-icon.png" alt="Edit Profile Picture" onclick="document.getElementById('profilePic').click()">
    
    <div class="input-field">
        <label for="name">Name:</label>
        <input type="text" id="name" placeholder="Name">
    </div>
    
    <div class="input-field">
        <label for="username">Username:</label>
        <input type="text" id="username" placeholder="Username">
    </div>
    
    <input type="file" id="profilePic" accept="image/*" style="display:none;" onchange="changeProfileIcon(event)">
    
    <button onclick="saveProfile()">Save Changes</button>
</div>

<script>
    function changeProfileIcon(event) {
        const file = event.target.files[0];
        const reader = new FileReader();
        reader.onload = function(e) {
            document.getElementById('profileIcon').src = e.target.result;
        };
        reader.readAsDataURL(file);
    }

    function saveProfile() {
        const name = document.getElementById('name').value;
        const username = document.getElementById('username').value;
        
        alert(`Profile Updated:\nName: ${name}\nUsername: ${username}`);
    }
</script>

</body>

