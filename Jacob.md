---
toc: false
comments: false
layout: tailwind
title: V-Card
description: Digital business card with contact information
type: hacks
permalink: /vcard
---
<div class="bg-gradient-to-br from-blue-50 to-white min-h-screen flex flex-col items-center justify-center p-6 space-y-8">
  <!-- Profile Photo -->
  <div class="w-64 h-64 transform hover:scale-[1.02] transition-transform duration-300">
    <img src="https://via.placeholder.com/400x400.png?text=Jacob+Zierolf" alt="Profile Photo" class="rounded-2xl shadow-xl w-full h-full object-cover object-center" />
  </div>
  <!-- Card Section -->
  <div class="flex flex-col lg:flex-row gap-8 w-full max-w-5xl">
    <!-- Left Card - Contact Info -->
    <div class="flex-1 bg-white rounded-2xl border border-red-200 shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
      <div class="space-y-6">
        <h3 class="text-2xl font-bold text-gray-800 text-center mb-6">Contact Information</h3>
        <div class="grid grid-cols-1 gap-4 text-gray-700">
          <a href="mailto:jake.zierolf@gmail.com" class="flex items-center gap-3 p-3 rounded-lg hover:bg-red-50 transition-colors duration-200">
            <img src="https://img.icons8.com/color/24/gmail.png" alt="Gmail" class="w-6 h-6"/>
            <span class="font-medium">jake.zierolf@gmail.com</span>
          </a>
          <a href="#" class="flex items-center gap-3 p-3 rounded-lg hover:bg-red-50 transition-colors duration-200">
            <img src="https://img.icons8.com/fluency/24/domain.png" alt="Website" class="w-6 h-6"/>
            <span class="font-medium">Portfolio Website (Coming Soon)</span>
          </a>
          <a href="https://www.linkedin.com/in/jacobzierolf" target="_blank" class="flex items-center gap-3 p-3 rounded-lg hover:bg-red-50 transition-colors duration-200">
            <img src="https://img.icons8.com/color/24/linkedin.png" alt="LinkedIn" class="w-6 h-6"/>
            <span class="font-medium">LinkedIn Profile</span>
          </a>
          <a href="https://github.com/jacobcancode" target="_blank" class="flex items-center gap-3 p-3 rounded-lg hover:bg-red-50 transition-colors duration-200">
            <img src="https://img.icons8.com/material-outlined/24/github.png" alt="GitHub" class="w-6 h-6"/>
            <span class="font-medium">GitHub Profile</span>
          </a>
        </div>
        <!-- Download vCard Button -->
        <div class="pt-4 text-center">
          <button onclick="downloadVCard()" class="bg-red-600 hover:bg-red-700 text-white font-bold py-3 px-6 rounded-lg transition-colors duration-200 shadow-md hover:shadow-lg transform hover:scale-105">
            📄 Download vCard
          </button>
        </div>
      </div>
    </div>
    <!-- Right Card - QR Code -->
    <div class="flex-1 bg-white rounded-2xl border border-red-200 shadow-lg p-8 hover:shadow-xl transition-shadow duration-300 flex flex-col items-center justify-center space-y-6">
      <div class="text-center space-y-4">
        <h3 class="text-2xl font-bold text-gray-800">Quick Connect</h3>
      </div>
      <!-- QR Codes Container -->
      <div class="flex flex-col gap-6 items-center justify-center">
        <!-- vCard Page QR Code -->
        <div class="text-center space-y-2">
          <div class="transform hover:scale-105 transition-transform duration-300">
            <img src="https://via.placeholder.com/200x200.png?text=vCard+QR" alt="vCard QR Code" class="w-48 h-48 rounded-xl shadow-md border border-gray-200" />
          </div>
          <p class="text-sm text-gray-600 font-medium">This Page</p>
        </div>
        <!-- Main Website QR Code -->
        <div class="text-center space-y-2">
          <div class="transform hover:scale-105 transition-transform duration-300">
            <img src="https://via.placeholder.com/200x200.png?text=Website+QR" alt="Website QR Code" class="w-48 h-48 rounded-xl shadow-md border border-gray-200" />
          </div>
          <p class="text-sm text-gray-600 font-medium">Portfolio Website</p>
        </div>
      </div>
    </div>
  </div>
</div>

<script>
function downloadVCard() {
  const vCardData = `BEGIN:VCARD
VERSION:3.0
FN:Jacob Zierolf
EMAIL:jake.zierolf@gmail.com
URL:https://github.com/jacobcancode
NOTE:Connect with me on LinkedIn and GitHub!
END:VCARD`;
  const blob = new Blob([vCardData], { type: 'text/vcard' });
  const url = window.URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = 'JacobZierolf_contact.vcf';
  document.body.appendChild(a);
  a.click();
  document.body.removeChild(a);
  window.URL.revokeObjectURL(url);
}
</script>
