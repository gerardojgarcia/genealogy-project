<script setup lang="ts">
const tiers = [
  {
    name: 'Starter',
    price: '$300',
    features: [
      'Pedigree chart (up to 3 generations) with basic relationship insights',
      'One historical record lookup (e.g., birth or marriage certificate)',
      'High-level research summary report'
    ]
  },
  {
    name: 'Essentials',
    price: '$750',
    features: [
      'Pedigree chart (up to 5 generations) with detailed relationship analysis',
      'Retrieval of up to 3 vital or census records',
      'Annotated timeline of key family events'
    ]
  },
  {
    name: 'Comprehensive',
    price: '$1,500',
    features: [
      'Pedigree chart (up to 10 generations) with full network visualization',
      'Retrieval of up to 7 archival documents (vital, census, wills, land records)',
      'DNA integration report: convergence of genetic matches with paper trail',
      'Research narrative (5–7 pages)'
    ]
  },
  {
    name: 'Legacy',
    price: '$2,500',
    features: [
      'Unlimited-generation pedigree and collateral kin charts',
      'Unlimited record retrieval from multiple repositories (up to 15 items)',
      'In-depth DNA + documentary synthesis report',
      'Heirloom preservation plan & restoration guidance',
      '60‑min strategy call to review findings and next steps'
    ]
  }
];
</script>

<template>
  <section class="bg-gray-50 py-16">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-gray-900 mb-8">Service Tiers</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div
            v-for="tier in tiers"
            :key="tier.name"
            class="bg-white rounded-xl p-6 flex flex-col justify-between hover:shadow-xl transition-shadow"
        >
          <div>
            <h3 class="text-2xl font-semibold text-blue-600 mb-2">{{ tier.name }}</h3>
            <p class="text-3xl font-bold text-gray-900 mb-4">{{ tier.price }}</p>
            <ul class="text-gray-600 space-y-2 mb-6 list-disc list-inside">
              <li v-for="(feature, idx) in tier.features" :key="idx">
                {{ feature }}
              </li>
            </ul>
          </div>
          <button class="mt-4 bg-blue-600 text-white px-4 py-2 rounded-full hover:bg-blue-700 transition self-start">
            Get Started
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>