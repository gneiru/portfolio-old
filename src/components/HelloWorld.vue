<script setup>
import health from '../assets/health.png'
import orca from '../assets/orca.png'
import calc from '../assets/calc.png'
import cgs from '../assets/cgs.png'
import raidmap from '../assets/raidmap.png'
import gt from '../assets/gt.png'


defineProps({
  name: String
})

</script>

<template>
  <div class="text-3xl">gneiru</div>
  <div class="text-lg">Welcome to my website</div>
  <button class="button" onclick="location.href='src/assets/resume.docx';">Download Resume</button>
  <div class="flex flex-col ">
    <div class="bg-[#3E4451] m-4 p-2 rounded-lg shadow-lg shadow-cyan-500/50">
      <div class="text-3xl text-yellow-400">About Me</div>
      <p class="">I'm {{name}}, a developer from Pangasinan, 23 years old, and an open-source enthusiast</p>
    </div>
    <div class="bg-[#3E4451] m-4 p-2 rounded-lg shadow-lg shadow-cyan-500/50">
      <div class="text-3xl text-yellow-400">Languages & technologies</div>
      <div class="m-2">
        JavaScript
        Python
        Php
        C++
        
      </div>
      <div class="m-2">
        Vue.js
        Django
        FastAPI
        TailwindCSS
      </div>
    </div>
    <div class="bg-[#3E4451] m-4 p-2 rounded-lg shadow-lg shadow-cyan-500/50">
      <div class="text-3xl text-yellow-400">Projects</div>
      <div class="grid grid-cols-2">
      <span class="bg-[#3C4049] m-5 shadow-inner shadow-cyan-500/50 rounded-lg">
        <div class="text-lg ">Personal Health Care Guide</div>
        <a href="http://youtube.com/watch?v=_PT9XjHJU2M" target="_blank" rel="noopener noreferrer">
          <img :src="health" alt="" class="p-2">
        </a>
      </span>
      <span class="bg-[#3C4049] m-5 shadow-inner shadow-cyan-500/50 rounded-lg">
        <div class="text-lg ">Child Growth Monitoring and Malnutrition System</div>
        <a :href="cgs" target="_blank" rel="noopener noreferrer">
          <img :src="cgs" alt="" class="p-2">
        </a>
      </span>
      <span class="bg-[#3C4049] m-5 shadow-inner shadow-cyan-500/50 rounded-lg">
        <div class="text-lg">Bounty Experience Calculator</div>
        <a href="https://gneiru.github.io/vite-exp-calculator/" target="_blank" rel="noopener noreferrer">
          <img :src="calc" alt="" class="p-2">
        </a>
      </span >
      <span class="bg-[#3C4049] m-5 shadow-inner shadow-cyan-500/50 rounded-lg">
        <div class="text-lg">Raid Map Generator</div>
        <a href="https://gneiru.github.io/raid-maps/" target="_blank" rel="noopener noreferrer">
          <img :src="raidmap" alt="" class="p-2">
        </a>
      </span>
      <span class="bg-[#3C4049] m-5 shadow-inner shadow-cyan-500/50 rounded-lg">
        <div class="text-lg">Guardian Tales Heroes</div>
        <a href="https://gneiru.github.io/gt-search/" target="_blank" rel="noopener noreferrer">
          <img :src="gt" alt="" class="p-2">
        </a>
      </span>
      <span class="bg-[#3C4049] m-5 shadow-inner shadow-cyan-500/50 rounded-lg">
        <div class="text-lg">Orca Discord Bot</div>
        <a href="https://shidou-bot.github.io/" target="_blank" rel="noopener noreferrer">
          <img :src="orca" alt="" class="p-2">
        </a>
      </span>
      </div>
      <div class="bg-[#3E4451] m-4 p-2 rounded-lg shadow-lg shadow-cyan-500/50">
        <div class="text-3xl text-yellow-400 mb-4">Socials</div>
        <div class="m-auto">
          <a href="https://facebook.com/noel.rohi" class="m-2 text-black hover:text-white">Facebook</a>
          <a href="https://linkedin.com/in/gneiru" class="m-2 text-black hover:text-white">LinkedIn</a>
          <a href="https://github.com/gneiru" class="m-2 text-black hover:text-white">Github</a>
          <a href="https://instagram.com/nelrohg" class="m-2 text-black hover:text-white">Instagram</a>
        </div>
      </div>
      

    </div>
  </div>
</template>

<style scoped>
</style>
