<script setup lang="ts">
import { ref, computed } from 'vue';

import { ChevronLeftIcon, ChevronRightIcon } from '@heroicons/vue/24/outline';
const projects = [
  {
    id: 1,
    image: '/gene-5.png',
    alt: 'Family tree mapping',
    title: 'Century-Old Lineage Revealed',
    description: 'Traced a family line back to the 1800s, uncovering lost ancestors and vital records.',
    tags: ['Pedigree Charts', 'Census Records', 'Archival Research']
  },
  {
    id: 2,
    image: '/gene-2.png',
    alt: 'Historical document retrieval',
    title: 'Lost Birth Certificates Found',
    description: 'Recovered missing birth and marriage certificates from state archives for three generations.',
    tags: ['Vital Records', 'Archive Access', 'Document Restoration']
  },
  {
    id: 3,
    image: '/gene-4.png',
    alt: 'DNA integration analysis',
    title: 'Genetic & Paper Trail Aligned',
    description: 'Integrated DNA matches with documented evidence to verify family connections with precision.',
    tags: ['DNA Analysis', 'Family Matches', 'Record Correlation']
  },
  {
    id: 4,
    image: '/gene-5.png',
    alt: 'Heirloom preservation',
    title: 'Heirlooms Digitally Preserved',
    description: 'Digitized and cataloged over 200 family photos and letters, ensuring their legacy.',
    tags: ['Digitization', 'Photo Restoration', 'Metadata']
  }
];

const currentIndex = ref(0);
const slidesToShow = 3;
const total = projects.length;

const carouselStyle = computed(() => {
  const offset = (currentIndex.value * (100 / slidesToShow));
  return { transform: `translateX(-${offset}%)` };
});

function next() {
  currentIndex.value = (currentIndex.value + 1) % total;
}

function prev() {
  currentIndex.value = (currentIndex.value - 1 + total) % total;
}
</script>

<template>
  <section class="bg-white py-16">
    <div class="container mx-auto  p-16">
      <span class="inline-block text-sm font-medium text-gray-500 uppercase tracking-wide mb-2">
        Portfolio
      </span>
      <div class="flex justify-between items-center mb-8">
        <h2 class="text-3xl font-bold text-gray-900">
          Our success stories: Real results, real impact
        </h2>

      </div>

      <div class="relative overflow-hidden bg-gray-100 rounded-xl py-16">
        <!-- Carousel Track -->
        <div
            class="flex transition-transform duration-500"
            :style="carouselStyle"
        >
          <div
              v-for="project in projects"
              :key="project.id"
              class="group flex-shrink-0 w-full md:w-1/3 px-4"
          >
            <div class="bg-white rounded-lg overflow-hidden group-hover:shadow-2xl group-hover:scale-105 transition-all duration-300">
              <div class="overflow-hidden">
                <img
                    :src="project.image"
                    :alt="project.alt"
                    class="w-full h-48 object-cover transition-transform duration-300 group-hover:scale-105"
                />
              </div>
              <div class="p-6">
                <h3 class="text-xl font-semibold text-gray-900 mb-2">
                  {{ project.title }}
                </h3>
                <p class="text-gray-600 mb-4">
                  {{ project.description }}
                </p>
                <div class="flex flex-wrap">
                  <span
                      v-for="tag in project.tags"
                      :key="tag"
                      class="inline-block bg-blue-100 text-blue-600 text-xs font-medium mr-2 mb-2 px-2.5 py-0.5 rounded"
                  >
                    {{ tag }}
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Arrows -->
        <button
            @click="prev"
            class="absolute left-0 top-1/2 transform -translate-y-1/2 bg-white p-2 rounded-full shadow hover:shadow-md"
        >
          <ChevronLeftIcon class="h-6 w-6 text-gray-700" />
        </button>
        <button
            @click="next"
            class="absolute right-0 top-1/2 transform -translate-y-1/2 bg-white p-2 rounded-full shadow hover:shadow-md"
        >
          <ChevronRightIcon class="h-6 w-6 text-gray-700" />
        </button>
      </div>
    </div>
  </section>
</template>

<style scoped>

.container {
  touch-action: pan-y;
}

</style>