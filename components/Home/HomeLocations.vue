<template>
  <div class="def-container def-margin">
    <!-- Header -->
    <div class="text-center mb-16">
      <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
        Our Global Presence
      </h2>
    </div>

    <!-- Description and Button Section -->
    <div class="flex flex-col lg:flex-row lg:items-center justify-between mb-12 gap-6">
      <div class="lg:max-w-2xl">
        <p class="text-lg text-gray-600 leading-relaxed">
          With offices strategically located across three continents, we deliver world-class services to clients
          globally. Our international presence ensures we understand diverse markets and can provide localized solutions
          while maintaining consistent quality standards.
        </p>
      </div>
      <div class="flex-shrink-0">
        <button @click="$emit('openModal')"
          class="cursor-pointer  bg-[#E2725B] hover:bg-[#d1634a] text-white px-8 py-4 rounded-full font-medium transition-all
          duration-300 hover:shadow-lg transform hover:-translate-y-1">
          Contact Our Offices
        </button>
      </div>
    </div>

    <!-- Locations Grid -->
    <div class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 gap-8">
      <!-- Dubai Card -->
      <div class="group cursor-pointer">
        <div
          class="bg-[#E2725B] hover:bg-[#d1634a] transition-all duration-500 md:rounded-4xl rounded-2xl relative overflow-hidden h-[400px]">
          <div class="absolute top-10 left-10 flex flex-col gap-4 text-white z-10">
            <h4 class="md:text-5xl text-3xl font-bold">
              Dubai
            </h4>
            <p class="text-lg opacity-90">United Arab Emirates</p>
            <div class="mt-4 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
              <div class="flex items-center gap-2 text-sm">
                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd"
                    d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z"
                    clip-rule="evenodd" />
                </svg>
                <span>Business Bay, Dubai</span>
              </div>
            </div>
          </div>
          <img src="/dub.png"
            class="absolute bottom-0 right-0 h-full object-cover opacity-20 group-hover:opacity-30 transition-opacity duration-500"
            alt="Dubai Office">
          <div class="absolute inset-0 bg-gradient-to-br from-[#E2725B]/80 to-[#d1634a]/60"></div>
        </div>
      </div>

      <!-- New York Card -->
      <div class="group cursor-pointer">
        <div
          class="bg-[#E2725B] hover:bg-[#d1634a] transition-all duration-500 md:rounded-4xl rounded-2xl relative overflow-hidden h-[400px]">
          <div class="absolute top-10 left-10 flex flex-col gap-4 text-white z-10">
            <h4 class="md:text-5xl text-3xl font-bold">
              New York
            </h4>
            <p class="text-lg opacity-90">United States of America</p>
            <div class="mt-4 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
              <div class="flex items-center gap-2 text-sm">
                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd"
                    d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z"
                    clip-rule="evenodd" />
                </svg>
                <span>Manhattan, New York</span>
              </div>
            </div>
          </div>
          <img src="/ny.png"
            class="absolute bottom-0 right-0 h-full object-cover opacity-20 group-hover:opacity-30 transition-opacity duration-500"
            alt="New York Office">
          <div class="absolute inset-0 bg-gradient-to-br from-[#E2725B]/80 to-[#d1634a]/60"></div>
        </div>
      </div>

      <!-- Karachi Card -->
      <div class="group cursor-pointer">
        <div
          class="bg-[#E2725B] hover:bg-[#d1634a] transition-all duration-500 md:rounded-4xl rounded-2xl relative overflow-hidden h-[400px]">
          <div class="absolute top-10 left-10 flex flex-col gap-4 text-white z-10">
            <h4 class="md:text-5xl text-3xl font-bold">
              Karachi
            </h4>
            <p class="text-lg opacity-90">Pakistan</p>
            <div class="mt-4 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
              <div class="flex items-center gap-2 text-sm">
                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd"
                    d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z"
                    clip-rule="evenodd" />
                </svg>
                <span>Clifton, Karachi</span>
              </div>
            </div>
          </div>
          <img src="/khi.png"
            class="absolute bottom-0 right-0 h-full object-cover opacity-20 group-hover:opacity-30 transition-opacity duration-500"
            alt="Karachi Office">
          <div class="absolute inset-0 bg-gradient-to-br from-[#E2725B]/80 to-[#d1634a]/60"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>


/* Additional hover effects */
.group:hover .transform {
  transform: translateY(-2px);
}

/* Smooth gradient overlay */
.bg-gradient-to-br {
  background: linear-gradient(to bottom right, var(--tw-gradient-stops));
}
</style>