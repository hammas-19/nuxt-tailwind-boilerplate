<template>
  <nav
    class="fixed top-0 py-4 left-0 w-full z-50 bg-gradient-to-b backdrop-blur-sm from-[#ffffff] via-[#ffffff9f] to-[#ffffff17]">
    <div class="def-container mx-auto">
      <div class="bg-peachy rounded-full px-1 pl-6 py-3 shadow-lg">
        <div class="flex items-center justify-between h-12">
          <!-- Logo -->
          <div class="flex-shrink-0">
              <a href="/#home" class="text-white font-bold text-xl">
              <img src="/techLabsLogo.png" class="w-fit max-w-[50px]" alt="Mr TechLabs">
              </a>
          </div>

          <!-- Desktop Navigation -->
          <div class="hidden md:block">
            <div class="ml-10 flex items-baseline space-x-6">
               <a href="/#home"
                class="text-white hover:text-white/80 px-2 py-1 text-sm md:text-xl font-medium transition-colors duration-200">
                Home
            </a>
              <a href="/#aboutus"
                class="text-white hover:text-white/80 px-2 py-1 text-sm md:text-xl font-medium transition-colors duration-200">
                About us
              </a>
              <a href="/#services"
                class="text-white hover:text-white/80 px-2 py-1 text-sm md:text-xl font-medium transition-colors duration-200">
                Services
              </a>
              <a href="/#portfolio"
                class="text-white hover:text-white/80 px-2 py-1 text-sm md:text-xl font-medium transition-colors duration-200">
                Portfolio
              </a>
              <a href="/#testimonials"
                class="text-white hover:text-white/80 px-2 py-1 text-sm md:text-xl font-medium transition-colors duration-200">
                Testimonials
              </a>
            </div>
          </div>

          <!-- Contact Us Button -->
          <div class="hidden md:block">
            <button @click="$emit('openModal')"
              class="bg-white border border-white text-peachy hover:bg-transparent hover:text-white px-8 py-4 rounded-full font-medium transition-all duration-200 text-sm md:text-xl">
              Contact Us
            </button>
          </div>

          <!-- Mobile menu button -->
          <div class="md:hidden">
            <button @click="toggleMobileMenu"
              class="text-white hover:text-white/80 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white mr-5">
              <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16" />
                <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
              </svg>
            </button>
          </div>
        </div>
      </div>

      <!-- Mobile Navigation Menu -->
      <div v-show="mobileMenuOpen" class="md:hidden mt-2">
        <div class="bg-peachy rounded-2xl px-4 py-4 space-y-2 shadow-lg">
           <a href="/#home"
            class="text-white hover:text-white/80 block px-3 py-2 text-sm font-medium transition-colors duration-200"
            @click="closeMobileMenu">
            Home
        </a>
          <a href="/#aboutus"
            class="text-white hover:text-white/80 block px-3 py-2 text-sm font-medium transition-colors duration-200"
            @click="closeMobileMenu">
            About us
          </a>
          <a href="/#services"
            class="text-white hover:text-white/80 block px-3 py-2 text-sm font-medium transition-colors duration-200"
            @click="closeMobileMenu">
            Services
          </a>
          <a href="/#portfolio"
            class="text-white hover:text-white/80 block px-3 py-2 text-sm font-medium transition-colors duration-200"
            @click="closeMobileMenu">
            Portfolio
          </a>
          <a href="/#testimonials"
            class="text-white hover:text-white/80 block px-3 py-2 text-sm font-medium transition-colors duration-200"
            @click="closeMobileMenu">
            Testimonials
          </a>
          <button @click="() => { $emit('openModal'); closeMobileMenu(); }"
            class="bg-white border border-white text-peachy hover:bg-transparent hover:text-white block px-3 py-2 rounded-full text-sm font-medium transition-all duration-200 mt-3 text-center w-full">
            Contact Us
          </button>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
// Define the emit function
const emit = defineEmits(['openModal'])

const mobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

const closeMobileMenu = () => {
  mobileMenuOpen.value = false
}
</script>