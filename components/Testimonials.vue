<script setup lang="ts">
import { ref, computed } from 'vue';
import { ChevronLeftIcon, ChevronRightIcon } from '@heroicons/vue/24/outline';

const testimonials = [
  {
    id: 1,
    image: '/test-woman-2.png',
    quote: 'They brought clarity to complex family histories and guided me every step of the way. I couldn’t be happier with the results.',
    name: 'Maria Hernandez',
    role: 'Entrepreneur'
  },
  {
    id: 2,
    image: '/testimonial-man.png',
    quote: 'Their meticulous research uncovered records we thought were lost forever. A truly outstanding genealogy service.',
    name: 'James O’Connor',
    role: 'Historian'
  },
  {
    id: 3,
    image: '/testimonial-woman.png',
    quote: 'Thanks to their expertise, our family tree is richer and more accurate than ever. Highly recommended!',
    name: 'Heather Burk',
    role: 'Teacher'
  },
  {
    id: 4,
    image: '/testimonial-man-2.png',
    quote: 'Integrating DNA data with archival records was seamless and enlightening. They exceeded all expectations.',
    name: 'David Newman',
    role: 'Researcher'
  },

];

const currentIndex = ref(0);
const total = testimonials.length;

const carouselStyle = computed(() => ({ transform: `translateX(-${currentIndex.value * 100}%)` }));

function next() {
  currentIndex.value = (currentIndex.value + 1) % total;
}

function prev() {
  currentIndex.value = (currentIndex.value - 1 + total) % total;
}
</script>

<template>
  <section class="bg-gray-50 py-16">
    <div class="container mx-auto px-6">
      <div class="max-w-2xl mx-auto text-center">
        <span class="inline-block text-sm font-medium text-gray-500 uppercase tracking-wide mb-2">
          Testimonials
        </span>
        <h2 class="text-3xl font-bold text-gray-900 mb-8">
          What our clients say
        </h2>
      </div>

      <div class="relative overflow-hidden">
        <!-- Carousel Track -->
        <div class="flex transition-transform duration-500" :style="carouselStyle">
          <div
              v-for="testimonial in testimonials"
              :key="testimonial.id"
              class="flex-shrink-0 w-full px-4"
          >
            <div class="bg-white p-8 rounded-lg shadow-sm flex shadow-xl flex-col items-center text-center w-3/4 m-auto">
              <img
                  :src="testimonial.image"
                  :alt="testimonial.name"
                  class="w-24 h-24 rounded-full mb-6 object-cover"
              />
              <strong class="text-lg italic text-gray-700 mb-6">
                “{{ testimonial.quote }}”
              </strong>
              <p class="font-semibold text-gray-900">{{ testimonial.name }}</p>
              <p class="text-sm text-gray-500">{{ testimonial.role }}</p>
            </div>
          </div>
        </div>

        <!-- Arrows -->
        <div class="flex justify-center mt-8 space-x-4">
          <button
              @click="prev"
              class="p-3 border-2 border-blue-600 text-blue-600 rounded-full hover:bg-blue-50 focus:outline-none"
          >
            <ChevronLeftIcon class="h-5 w-5" />
          </button>
          <button
              @click="next"
              class="p-3 border-2 border-blue-600 text-blue-600 rounded-full hover:bg-blue-50 focus:outline-none"
          >
            <ChevronRightIcon class="h-5 w-5" />
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.container {
  touch-action: pan-y;
}
</style>