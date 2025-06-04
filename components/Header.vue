<script setup lang="ts">
import { ref } from 'vue';

const navLinks = [
  { text: 'Home ', href: '/' },
  { text: 'About ', href: '#about' },
  { text: 'Services', href: '#services' },

];

const pages = [
  { text: 'Page 1', href: '#' },
  { text: 'Page 2', href: '#' },
  { text: 'Page 3', href: '#' }
];

const showPages = ref(false);
const mobileMenu = ref(false);
</script>

<template>
<header class="top-0 fixed w-full">

  <!-- Navigation -->
  <nav class="bg-white py-4 shadow">
    <div class="container mx-auto px-6 flex justify-between items-center">
      <!-- Logo -->
      <div class="flex items-center">
        <img src="/gene-1.png" alt="Navis Logo" class="h-8 w-8 mr-2" />
        <span class="text-xl font-bold">Mecayotl</span>
      </div>
      <!-- Links -->
      <ul class="hidden md:flex items-center space-x-6">
        <li v-for="link in navLinks" :key="link.text">
          <a :href="link.href" class="text-gray-700 hover:text-gray-900">{{ link.text }}</a>
        </li>
        <!--<li class="relative" @mouseleave="showPages = false">
          <button @click="showPages = !showPages" class="flex items-center text-gray-700 hover:text-gray-900 focus:outline-none">
            Pages
            <svg class="ml-1 h-4 w-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <ul v-if="showPages" class="absolute top-full mt-2 bg-white shadow-lg rounded">
            <li v-for="page in pages" :key="page.text">
              <a :href="page.href" class="block px-4 py-2 text-gray-700 hover:bg-gray-100">{{ page.text }}</a>
            </li>
          </ul>
        </li> -->

        <li>
          <a href="#contact" class="bg-blue-600 text-white px-4 py-2 rounded-full hover:bg-blue-700">Contact</a>
        </li>
      </ul>
      <!-- Mobile Menu Toggle -->
      <button class="md:hidden focus:outline-none" @click="mobileMenu = !mobileMenu">
        <svg v-if="!mobileMenu" class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg v-else class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>
    <!-- Mobile Menu -->
    <div v-if="mobileMenu" class="md:hidden bg-white px-6 py-4">
      <ul class="space-y-4">
        <li v-for="link in navLinks" :key="link.text">
          <a :href="link.href" class="block text-gray-700 hover:text-gray-900">{{ link.text }}</a>
        </li>
        <li>

          <ul v-if="showPages" class="mt-2 space-y-2">
            <li v-for="page in pages" :key="page.text">
              <a :href="page.href" class="block text-gray-700 hover:text-gray-900">{{ page.text }}</a>
            </li>
          </ul>
        </li>


      </ul>
    </div>
  </nav>
</header>
</template>

<style scoped>

</style>