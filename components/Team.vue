<script setup lang="ts">

</script>

<template>
  <section class="bg-gray-50 py-16">
    <div class="container mx-auto px-6">

      <h4 class="text-3xl font-bold text-gray-900 mb-8">
        Meet Our Team
      </h4>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 md:mx-32">
        <!-- Jennifer Payan Card -->
        <div
            class="relative bg-white rounded-xl overflow-hidden group h-[55vh]"
        >
          <img
              src="/headshot_2.webp"
              alt="Jennifer Payan"
              class="w-full h-full object-cover transition-opacity duration-300"
          />
          <!-- Overlay on hover -->
          <div
              class="absolute inset-0 bg-blue-600 bg-opacity-90 flex flex-col justify-center items-center text-center px-6 opacity-0 group-hover:opacity-100 transition-opacity duration-300"
          >
            <h3 class="text-2xl font-semibold text-white mb-2">Jennifer Payan</h3>
            <p class="text-sm text-blue-100 mb-4">Owner & Chief Genealogist</p>
            <p class="text-sm text-blue-100">
              Jennifer has over a decade of experience guiding families through archival research in Mexico and the U.S. As an MLIS graduate specializing in archival studies, she leads projects in pedigree mapping, records retrieval, and digitization.
            </p>

            <!--
            <div class="flex space-x-4 mt-6">
              <a href="#" aria-label="LinkedIn" class="text-blue-100 hover:text-white">
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 ..." />
                </svg>
              </a>
              <a href="#" aria-label="Twitter" class="text-blue-100 hover:text-white">
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M24 4.557c-..." />
                </svg>
              </a>
              <a href="#" aria-label="Instagram" class="text-blue-100 hover:text-white">
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 2.163c3.204 0 3.584..." />
                </svg>
              </a>
            </div> -->
          </div>
          <!-- Name & Title at bottom -->
          <div class="absolute bottom-0 left-0 right-0  p-6">
            <h3 class="text-xl font-semibold text-white">Jennifer Payan</h3>
            <p class="text-sm text-gray-200">Owner & Chief Genealogist</p>
          </div>
        </div>

        <!-- Gerardo Garcia Card -->
        <div
            class="relative bg-white rounded-xl overflow-hidden group h-[55vh]"
        >
          <img
              src="/picpic.jpg"
              alt="Gerardo Garcia"
              class="w-full h-full object-cover transition-opacity duration-300"
          />
          <!-- Overlay on hover -->
          <div
              class="absolute inset-0 bg-blue-600 bg-opacity-90 flex flex-col justify-center items-center text-center px-6 opacity-0 group-hover:opacity-100 transition-opacity duration-300"
          >
            <h3 class="text-2xl font-semibold text-white mb-2">Gerardo Garcia</h3>
            <p class="text-sm text-blue-100 mb-4">Genealogist</p>
            <p class="text-sm text-blue-100">
              Gerardo specializes in archival retrieval and document analysis, with expertise in land records and military archives from Jalisco and Guanajuato. He ensures accuracy in every step of the research process.
            </p>

            <!--
            <div class="flex space-x-4 mt-6">
              <a href="#" aria-label="LinkedIn" class="text-blue-100 hover:text-white">
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 ..." />
                </svg>
              </a>
              <a href="#" aria-label="Twitter" class="text-blue-100 hover:text-white">
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M24 4.557c-..." />
                </svg>
              </a>
              <a href="#" aria-label="Instagram" class="text-blue-100 hover:text-white">
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 2.163c3.204 0 3.584..." />
                </svg>
              </a>
            </div>-->
          </div>
          <!-- Name & Title at bottom -->
          <div class="absolute bottom-0 left-0 right-0  p-6">
            <h3 class="text-xl font-semibold text-white">Gerardo Garcia</h3>
            <p class="text-sm text-gray-200">Genealogist</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>