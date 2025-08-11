<script setup>
import { RouterLink } from 'vue-router';
import logo from '@/assets/logo/logo2.png';
</script>

<template>
  <footer  class=" bg-ro-dark-gray py-8 font-Poppins">
    <div class="container flex flex-col md:flex-row items-center">
      <div class="flex flex-1 flex-wrap items-center justify-center md:justify-start gap-8 sm:gap-12 md:gap-14">
        <h3 class="text-white text-3xl">
          <RouterLink :to="{ name: 'home' }" class="white"><img class=" h-12 w-auto" :src="logo" alt="" /></RouterLink>
        </h3>
        <ul class="flex flex-wrap justify-center text-white items-center uppercase gap-8 md:gap-12 text-md tracking-wide pt-1">
          <li class="cursor-pointer hover-underline-animation transition-duration:150ms white">
            <RouterLink :to="{ name: 'home' }">Home</RouterLink>
          </li>
          <li class="cursor-pointer hover-underline-animation transition-duration:150ms white">
            <RouterLink :to="{ name: 'about' }">About</RouterLink>
          </li>
          <li class="cursor-pointer hover-underline-animation transition-duration:150ms white">
            <RouterLink :to="{ name: 'activitati' }">Activitati</RouterLink>
          </li>
          <li class="cursor-pointer hover-underline-animation transition-duration:150ms white">
            <RouterLink :to="{ name: 'about' }">Contact</RouterLink>
          </li>
        </ul>
      </div>
      <div class="flex gap-10 mt-12 md:mt-0">
        <li>
          <a
            target="_blank"
            ><i
              class="text-white text-2xl pi pi-instagram hover:text-bookmark-purple hover:scale-105 transition-100 cursor-pointer"
            ></i
          ></a>
        </li>
        <li>
          <a
            target="_blank"
            ><i
              class="text-white text-2xl pi pi-facebook hover:text-bookmark-purple hover:scale-105 transition-100 cursor-pointer"
            ></i
          ></a>
        </li>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.white {
  color: white !important;
}
</style>