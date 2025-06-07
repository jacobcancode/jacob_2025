---
toc: false
comments: false
layout: tailwind
title: V-Card
description: Digital business card with contact information
type: hacks
permalink: /vcard
---
<div class="min-h-screen bg-gradient-to-br from-blue-50 to-white flex flex-col items-center justify-center px-6 py-10 space-y-10">
  <!-- Profile Section -->
  <div class="flex flex-col items-center space-y-4">
    <img src="" alt="" class="w-36 h-36 rounded-xl shadow-lg object-cover" />
    <h1 class="text-2xl font-bold text-gray-800">Jacob Zierolf</h1>
    <p class="text-sm text-gray-600">Full Stack Developer • Student • Creator</p>
  </div>
  <!-- Cards Grid -->
  <div class="grid grid-cols-1 md:grid-cols-2 gap-8 w-full max-w-4xl">
    <!-- Contact Info Card -->
    <div class="bg-white border border-gray-200 rounded-2xl shadow-lg p-6 flex flex-col justify-between">
      <h2 class="text-xl font-semibold text-gray-800 mb-4">Contact Information</h2>
      <ul class="space-y-3 text-gray-700 text-sm">
        <li class="flex items-center gap-2">
          <img src="https://img.icons8.com/color/24/gmail.png" />
          <a href="mailto:wendaobao@gmail.com" class="hover:underline">jake.zierolf@gmail.com</a>
        </li>
        <li class="flex items-center gap-2">
          <img src="https://img.icons8.com/material-outlined/24/github.png" />
          <a href="https://github.com/jacobcancode" target="_blank" class="hover:underline">GitHub Profile</a>
        </li>
        <li class="flex items-center gap-2">
          <img src="https://img.icons8.com/color/24/linkedin.png" />
          <a href="linkedin.com/in/jacobzierolf" target="_blank" class="hover:underline">LinkedIn Profile</a>
        </li>
        <li class="flex items-center gap-2">
        </li>
      </ul>
      <div class="pt-6 text-center">
        <script>
function downloadVCard() {
  // Create vCard data
  const vCardData = `
BEGIN:VCARD
VERSION:3.0
FN:Jacob Zierolf
EMAIL:jake.zierolf@gmail.com
URL:https://github.22com/jacobcancode
NOTE:Connect with me on LinkedIn and GitHub!
END:VCARD
  `.trim();


