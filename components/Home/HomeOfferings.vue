<template>
  <section class="py-20 bg-white">
    <div class="def-container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-20">

        <!-- Left Side - Sticky Content -->
        <div class="lg:sticky lg:top-32 lg:self-start">
          <div class="max-w-lg">
            <!-- Services Badge -->
            <div class="inline-block text-[#E2725B] font-semibold text-lg mb-4">
              Services
            </div>

            <!-- Main Heading -->
            <h2 class="text-4xl lg:text-5xl font-bold text-boss mb-6 leading-tight">
              What We Offer
            </h2>

            <!-- Description -->
            <p class="text-lg text-gray-600 leading-relaxed">
              We provide comprehensive design services to enhance your product's usability and visual appeal.
            </p>
          </div>
        </div>

        <!-- Right Side - Service Cards -->
        <div class="space-y-6">

          <!-- UX Audit Card -->
          <div
            class="bg-boss rounded-2xl p-8 text-white relative overflow-hidden group hover:transform hover:scale-105 transition-all duration-300">
            <!-- Number Badge -->
            <div class="text-[#E2725B] font-bold text-lg mb-4">01</div>

            <!-- Service Title -->
            <h3 class="text-3xl font-bold mb-4">UX Audit</h3>

            <!-- Service Description -->
            <p class="text-gray-300 text-lg leading-relaxed mb-6">
              We review your current design to find areas for improvement and make it more user-friendly.
            </p>

            <!-- Icon -->
            <div class="absolute top-8 right-8">
              <svg class="w-12 h-12 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                  d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                  d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
              </svg>
            </div>
          </div>

          <!-- Wireframing Card -->
          <div
            class="bg-boss rounded-2xl p-8 text-white relative overflow-hidden group hover:transform hover:scale-105 transition-all duration-300">
            <!-- Number Badge -->
            <div class="text-[#E2725B] font-bold text-lg mb-4">02</div>

            <!-- Service Title -->
            <h3 class="text-3xl font-bold mb-4">Wireframing</h3>

            <!-- Service Description -->
            <p class="text-gray-300 text-lg leading-relaxed mb-6">
              We create simple sketches of your app or website to plan the layout and user journey.
            </p>

            <!-- Icon -->
            <div class="absolute top-8 right-8">
              <svg class="w-12 h-12 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                  d="M4 5a1 1 0 011-1h14a1 1 0 011 1v2a1 1 0 01-1 1H5a1 1 0 01-1-1V5zM4 13a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H5a1 1 0 01-1-1v-6zM16 13a1 1 0 011-1h2a1 1 0 011 1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-6z" />
              </svg>
            </div>
          </div>

          <!-- Visual Design Card -->
          <div
            class="bg-boss rounded-2xl p-8 text-white relative overflow-hidden group hover:transform hover:scale-105 transition-all duration-300">
            <!-- Number Badge -->
            <div class="text-[#E2725B] font-bold text-lg mb-4">03</div>

            <!-- Service Title -->
            <h3 class="text-3xl font-bold mb-4">Visual Design</h3>

            <!-- Service Description -->
            <p class="text-gray-300 text-lg leading-relaxed mb-6">
              We design attractive and intuitive interfaces that users will love and find easy to use.
            </p>

            <!-- Icon -->
            <div class="absolute top-8 right-8">
              <svg class="w-12 h-12 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                  d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zM7 21h10a2 2 0 002-2v-5a2 2 0 00-2-2H9a2 2 0 00-2 2v7z" />
              </svg>
            </div>
          </div>

          <!-- Usability Testing Card -->
          <div
            class="bg-boss rounded-2xl p-8 text-white relative overflow-hidden group hover:transform hover:scale-105 transition-all duration-300">
            <!-- Number Badge -->
            <div class="text-[#E2725B] font-bold text-lg mb-4">04</div>

            <!-- Service Title -->
            <h3 class="text-3xl font-bold mb-4">Usability Testing</h3>

            <!-- Service Description -->
            <p class="text-gray-300 text-lg leading-relaxed mb-6">
              We test your product with real users to find and fix any problems, ensuring it works smoothly for
              everyone.
            </p>

            <!-- Icon -->
            <div class="absolute top-8 right-8">
              <svg class="w-12 h-12 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                  d="M15 15l-2 5L9 9l11 4-5 2zm0 0l5 5M7.188 2.239l.777 2.897M5.136 7.965l-2.898-.777M13.95 4.05l-2.122 2.122m-5.657 5.656l-2.12 2.122" />
              </svg>
            </div>
          </div>

        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
// No additional logic needed for this component
</script>

<style scoped>
/* Custom scrolling behavior for sticky positioning */
@media (min-width: 1024px) {
  .lg\:sticky {
    position: sticky;
  }
}
</style>