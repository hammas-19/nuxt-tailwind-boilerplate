<template>
  <section class="py-20 bg-[#E2725B]">
    <div class="def-container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center max-w-4xl mx-auto">

        <!-- Main Heading -->
        <h2 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-boss leading-tight mb-8">
          The Best Marketing Agency For Your Business With Proven Results
        </h2>

        <!-- Italic Subheading -->
        <p class="text-2xl sm:text-3xl text-white/90 font-medium italic mb-8">
          We're dedicated to helping local businesses succeed.
        </p>

        <!-- Description -->
        <p class="text-lg sm:text-xl text-white/80 leading-relaxed mb-12 max-w-3xl mx-auto">
          Explore our case studies and see how we've helped companies across the UK, offering expert advice every step
          of the way.
        </p>

        <!-- CTA Button -->
        <div class="flex justify-center">
          <button @click="$emit('openModal')"
            class="inline-flex items-center gap-3 bg-white text-[#E2725B] font-semibold py-4 px-8 rounded-full text-xl transition-all duration-300 ease-in-out transform translate-y-0 shadow-lg hover:bg-gray-50 hover:translate-y-[-0.25rem] hover:shadow-2xl">
            Let's Grow Together
            <div
              class="flex items-center justify-center w-8 h-8 bg-[#E2725B]/20 rounded-full transition-transform duration-300 ease-in-out hover:translate-x-1">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="w-5 h-5">
                <path
                  d="m18.707 12.707-3 3a1 1 0 0 1-1.414-1.414L15.586 13H6a1 1 0 0 1 0-2h9.586l-1.293-1.293a1 1 0 0 1 1.414-1.414l3 3a1 1 0 0 1 0 1.414z"
                  fill="#E2725B" />
              </svg>
            </div>
          </button>

        </div>

      </div>
    </div>
  </section>
</template>