<template>
  <section class="relative flex items-center bg-gradient-to-br from-gray-50 to-gray-100 overflow-hidden">

    <!-- Main Content Container -->
    <div class="mx-auto px-4 sm:px-6 lg:px-8 relative z-20">
      <div class="grid grid-cols-1 lg:grid-cols-5 gap-2 items-center min-h-[80vh] w-full">

        <!-- Left Side - Network Animation (Hidden on mobile) -->
        <div class="hidden lg:block h-full min-h-[500px] relative overflow-hidden">
          <HomeNetworkBg />
        </div>

        <!-- Center Content - Takes more space -->
        <div class="md:mt-36 mt-28 lg:col-span-3 flex items-center justify-center text-center md:py-[92px] py-16">
          <div class="max-w-2xl w-full">
            <!-- Top Badge -->
            <div
              class="inline-block bg-peachy text-white px-6 py-2 rounded-full text-sm font-medium mb-6 uppercase tracking-wide">
              Best Web Development Company for Success
            </div>

            <!-- Main Heading -->
            <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold leading-tight mb-6 text-gray-800">
              Transforming Ideas into<br>
              <span class="text-peachy">Digital Reality</span>
            </h1>

            <!-- Description -->
            <p class="text-lg sm:text-xl leading-relaxed text-gray-600 mb-10">
              We help businesses shine with custom web development,<br class="hidden sm:block">
              professional seo services, and creative design and branding services.<br class="hidden sm:block">
              Let's create something amazing together at <span class="text-peachy font-semibold">Mr</span> <span
                class="text-gray-800 font-bold">TechLabs</span>
            </p>

            <!-- CTA Button -->
            <div class="mt-8">
              <button
                class="inline-block bg-peachy hover:bg-[#d65a42] text-white font-semibold px-10 py-4 rounded-full text-lg transition-all duration-300 transform hover:-translate-y-1 hover:shadow-xl hover:shadow-peachy/30"
                @click="$emit('openModal')">
                Get Started
              </button>
            </div>
          </div>
        </div>

        <!-- Right Side - Image (Hidden on mobile) -->
        <div class="hidden lg:flex items-center justify-center h-full">
          <div class="relative w-full max-w-sm h-96 flex items-center justify-center">
            <img
              src="https://images.unsplash.com/photo-1451187580459-43490279c0fa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2072&q=80"
              alt="Digital transformation sphere"
              class="w-full h-full object-cover rounded-full shadow-2xl animate-bounce"
              style="animation: float 6s ease-in-out infinite;">
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { HomeNetworkBg } from '#components';

// No additional logic needed for this component
</script>

<style scoped>
@keyframes float {

  0%,
  100% {
    transform: translateY(0px);
  }

  50% {
    transform: translateY(-20px);
  }
}
</style>