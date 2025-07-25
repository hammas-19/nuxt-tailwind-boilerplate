<template>
  <div>
    <section class="my-20 relative overflow-hidden mx-5">
      <div class="max-w-7xl mx-auto rounded-[40px]  border-2 border-peachy">
        <div class="grid lg:grid-cols-2 gap-8 items-center justify-items-center overflow-hidden">

          <!-- Left Side - Image with Solar System Animation -->
          <div class=" bg-peachy rounded-4xl m-2 p-5 md:p-10">

            <!-- Badge -->
            <div class="mb-6">
              <span class=" text-white text-xl font-bold">Digital Transformation Services</span>
            </div>

            <!-- Main Heading -->
            <h2 class="text-2xl lg:text-4xl font-bold text-boss leading-tight mb-3">
              Your Digital Impression Matters
            </h2>

            <!-- Description -->
            <p class="text-white text-lg leading-relaxed mb-10">
              Our creative team at Mr TechLabs knows how important a strong online presence is. We work closely with
              you to understand your business, deliver solutions on time, and help your brand perform better online.
              From
              branding your business and developing your websites to marketing it effectively on social media and search
              engines, we
              do everything for your success.
            </p>

            <!-- Action Buttons -->
            <div class="flex flex-col sm:flex-row gap-6 items-start">
              <!-- Get In Touch Button -->
              <button @click="$emit('openModal')" class="about-cta-button border">
                Let's Grow Together
                <div class="about-cta-icon">
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="w-5 h-5">
                    <path
                      d="m18.707 12.707-3 3a1 1 0 0 1-1.414-1.414L15.586 13H6a1 1 0 0 1 0-2h9.586l-1.293-1.293a1 1 0 0 1 1.414-1.414l3 3a1 1 0 0 1 0 1.414z"
                      fill="#c9c9c9" />
                  </svg>
                </div>
              </button>

              <!-- Contact Info -->
              <div class="flex flex-col sm:flex-row sm:items-center gap-4">
                <div class="text-left">
                  <div class="text-xs text-white uppercase tracking-wide mb-1">CALL US AT</div>
                  <div class="font-bold text-gray-800">+971 582811612</div>
                </div>
              </div>
            </div>
          </div>
          <div class="flex justify-end relative">
            <img src="/CTA1/technical-development.png" alt="Website Development Showcase"
              class="w-fit h-full max-h-[450px] relative z-10 animate-float">
            <img src="/CTA1/Metallic-Puzzle.J03.png" class="metal-float h-[120px] w-fut absolute" alt="">
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
/* Custom button styles using theme colors */
.about-cta-button {
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  background-color: #E2725B;
  color: white;
  font-weight: 600;
  padding: 1rem 2rem;
  border-radius: 9999px;
  font-size: 1.125rem;
  transition: all 0.3s ease;
  transform: translateY(0);
  box-shadow: 0 4px 15px rgba(226, 114, 91, 0.3);
}

.about-cta-button:hover {
  background-color: #d65a42;
  transform: translateY(-0.25rem);
  box-shadow: 0 8px 25px rgba(226, 114, 91, 0.4);
}

.about-cta-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2rem;
  height: 2rem;
  background-color: rgba(255, 255, 255, 0.2);
  border-radius: 9999px;
  transition: transform 0.3s ease;
}

.about-cta-button:hover .about-cta-icon {
  transform: translateX(0.25rem);
}

@keyframes float {
  0% {
    transform: translateY(10px);
    /* Start at a small value */
  }

  50% {
    transform: translateY(-10px);
    /* Move up */
  }

  100% {
    transform: translateY(10px);
    /* Move back down */
  }
}

.animate-float {
  animation: float 8s ease-in-out infinite;
  /* Smooth animation with easing */
}
.metal-float {
  animation: float 5s ease-in-out infinite;
  /* Smooth animation with easing */
}
</style>