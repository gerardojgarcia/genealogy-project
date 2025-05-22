<script setup lang="ts">


const services = [
  {

    title: 'Family Tree Mapping',
    description: 'Visualize your ancestry with detailed pedigree charts and relationship insights.'
  },
  {

    title: 'Historical Records Retrieval',
    description: 'Locate and acquire vital records, census data, and archival documents.'
  },
  {

    title: 'DNA Integration',
    description: 'Combine genetic evidence with documented records for a complete heritage view.'
  },
  {

    title: 'Heirloom Preservation',
    description: 'Guidance on restoring and preserving family photographs, letters, and artifacts.'
  }
];
</script>

<template>
  <section class="bg-gray-50 py-16" id="services">
    <div class="container mx-auto px-6 flex flex-col md:flex-row  items-center">

      <!-- Services List -->
      <div class="md:w-1/2 order-1 md:order-2 mt-8 md:mt-0 md:p-8">
        <h2 class="text-3xl font-bold text-gray-900 mb-8">
          Explore our comprehensive service offerings
        </h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-8">
          <div v-for="service in services" :key="service.title" class="flex">
            <div class="flex-shrink-0">

            </div>
            <div class="ml-4">
              <h3 class="text-xl font-semibold text-gray-900">{{ service.title }}</h3>
              <p class="text-gray-600 mt-2">{{ service.description }}</p>
            </div>
          </div>
        </div>
      </div>
      <!-- Image -->
      <div class="md:w-1/2 order-2 md:order-1">
        <img
            src="/gene-4.png"
            alt="Genealogy services overview"
            class="w-full rounded-lg shadow-lg"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>