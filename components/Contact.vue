<script setup lang="ts">
import { reactive } from 'vue';
import { EnvelopeIcon, PhoneIcon, BuildingOffice2Icon } from '@heroicons/vue/24/outline';

const form = reactive({
  name: '',
  email: '',
  message: ''
});

function submitForm() {
  // Handle form submission, e.g., send to API
  console.log('Form submitted:', form);
  // Reset form
  form.name = '';
  form.email = '';
  form.message = '';
  alert('Thank you for reaching out! We will contact you soon.');
}
</script>

<template>
  <section class="bg-white py-16" id="contact">
    <div class="container mx-auto px-6 flex flex-col lg:flex-row gap-12">
      <!-- Contact Info -->
      <div class="lg:w-1/2">
        <span class="inline-block text-sm font-medium text-gray-500 uppercase tracking-wide mb-2">
          Contact Us
        </span>
        <h2 class="text-3xl font-bold text-gray-900 mb-6">
          Reach Out Today
        </h2>

        <div class="space-y-6 text-gray-700">
          <div class="flex items-center">
            <EnvelopeIcon class="h-6 w-6 text-blue-600 mr-3" />
            <div>
              <p class="text-sm font-medium">Email</p>
              <p>payanjennifer9@gmail.com</p>
            </div>
          </div>

          <div class="flex items-center">
            <PhoneIcon class="h-6 w-6 text-blue-600 mr-3" />
            <div>
              <p class="text-sm font-medium">Phone</p>
              <p>+1 (323) 270-7263</p>
            </div>
          </div>

          <!-- <div class="flex items-center">
            <BuildingOffice2Icon class="h-6 w-6 text-blue-600 mr-3" />
            <div>
              <p class="text-sm font-medium">Office</p>
              <p>789 Heritage Ln, Ancestry City, CA 90210</p>
            </div>
          </div> -->

          <div>
            <!-- <p class="text-sm font-medium mb-2">Follow Us</p>
             <div class="flex space-x-4"> -->
              <!-- Placeholder social icons
              <a href="#" aria-label="Facebook" class="text-gray-500 hover:text-blue-600">
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M22 12..." />
                </svg>
              </a>
              <a href="#" aria-label="LinkedIn" class="text-gray-500 hover:text-blue-600">
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M19 0h-14..." />
                </svg>
              </a>
              <a href="#" aria-label="Twitter" class="text-gray-500 hover:text-blue-600">
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M24 4.56..." />
                </svg>
              </a>
              <a href="#" aria-label="Instagram" class="text-gray-500 hover:text-blue-600">
                <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 2.163..." />
                </svg>
              </a>
            </div>-->
          </div>
        </div>
      </div>

      <!-- Contact Form -->
      <div class="lg:w-1/2">
        <form @submit.prevent="submitForm" class="space-y-6">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div>
              <label for="name" class="block text-sm font-medium text-gray-700 mb-1">Your Name</label>
              <input
                  v-model="form.name"
                  type="text"
                  id="name"
                  placeholder="Your name"
                  class="w-full border border-gray-300 rounded-full px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-600"
              />
            </div>
            <div>
              <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email address</label>
              <input
                  v-model="form.email"
                  type="email"
                  id="email"
                  placeholder="Your email address"
                  class="w-full border border-gray-300 rounded-full px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-600"
              />
            </div>
          </div>

          <div>
            <label for="message" class="block text-sm font-medium text-gray-700 mb-1">Message</label>
            <textarea
                v-model="form.message"
                id="message"
                rows="6"
                placeholder="Write something..."
                class="w-full border border-gray-300 rounded-xl px-4 py-3 focus:outline-none focus:ring-2 focus:ring-blue-600 resize-none"
            ></textarea>
          </div>

          <button
              type="submit"
              class="w-full bg-blue-600 text-white px-6 py-3 rounded-full hover:bg-blue-700 transition"
          >
            Submit
          </button>
        </form>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>