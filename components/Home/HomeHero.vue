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
        <div class="md:mt-36 mt-28 lg:col-span-3 flex items-center justify-center text-center pb-16 relative z-10">
          <div class="max-w-2xl w-full">
            <!-- Top Badge -->


            <!-- Main Heading -->
            <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold leading-tight mb-6 text-gray-800">
              YOUR SHORTCUT TO REVENUE ROCKETS <br>
              AND A ROCKSTAR BRAND

            </h1>

            <!-- Description -->
            <p class="text-lg sm:text-xl leading-relaxed text-gray-600 mb-10">
              We provide rapid, highly effective strategies to dramatically increase your sales and build a highly
              recognized, desirable brand.
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
          <div class="relative z-0 w-full  flex items-center justify-center">
            <img src="/misc/Our-Impact.png" alt="Digital transformation sphere"
              class="w-full object-cover h-[300px] xl:h-[380px] animate-spin-slow  overflow-visible">
          </div>
        </div>

      </div>
    </div>
  </section>
</template>


<style scoped>
/* Slow spinning animation */
@keyframes spin-slow {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}

.animate-spin-slow {
  animation: spin-slow 28s linear infinite;
}
</style>