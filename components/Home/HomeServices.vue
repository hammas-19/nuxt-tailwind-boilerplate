<template>
  <section class="py-20 bg-white">
    <div class=" mx-auto px-4 sm:px-6 lg:px-8">

      <!-- Header -->
      <div class="text-center mb-16">
        <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
          Services We Offer
        </h2>
        <p class="text-lg text-gray-600">
          We provide services from tech to design.
        </p>
      </div>

      <!-- Services Grid -->
      <div class="divide-y divide-gray-300">
        <div v-for="(service, index) in services" :key="index"
          class="group hover:bg-[#E2725B] transition-all duration-500 ease-in-out cursor-pointer">
          <div class="flex items-center justify-between py-8 px-6 lg:px-12 def-container">
            <div class="flex md:items-center md:gap-8 gap-4 lg:gap-12 md:flex-row flex-col">
              <!-- Service Image -->
              <div class="flex-shrink-0">
                <div class="w-20 h-20 lg:w-48 lg:h-24 rounded-full overflow-hidden">
                  <img :src="service.image" :alt="service.title" class="w-full h-full object-cover" />
                </div>
              </div>

              <!-- Service Content -->
              <div class="flex md:gap-10 gap-4 md:flex-row flex-col">
                <h3
                  class="text-2xl lg:text-3xl text-gray-900 group-hover:text-white mb-3 transition-colors duration-500">
                  {{ service.title }}
                </h3>
                <p class="text-gray-600 group-hover:text-white/90 text-base lg:text-lg transition-colors duration-500">
                  {{ service.description }}
                </p>
              </div>
            </div>

            <!-- Arrow Icon -->
            <div class="flex-shrink-0 ml-6">
              <div
                class="w-12 h-12 flex items-center justify-center bg-gray-100 group-hover:bg-white/20 rounded-full transition-all duration-500">
                <svg class="w-6 h-6 text-gray-600 !group-hover:text-white transition-colors duration-500"
                  xmlns="http://www.w3.org/2000/svg" width="32" height="32"
                  viewBox="0 0 24 24">
                  <path  d="M5 17.59L15.59 7H9V5h10v10h-2V8.41L6.41 19z" />
                </svg>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    title: "BRANDING & VISUAL IDENTITY",
    description: "Craft unique, eye-catching brands that distinctively elevate your business profile and market presence.",
    image: "https://images.unsplash.com/photo-1561070791-2526d30994b5?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "UX/UI RESEARCH & DESIGN",
    description: "Develop easy-to-use, engaging interfaces with deep user research to ensure satisfaction and usability.",
    image: "https://images.unsplash.com/photo-1581291518857-4e27b48ff24e?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "WEB & MOBILE APP DEVELOPMENT",
    description: "Build reliable digital products meticulously tailored to meet contemporary business needs.",
    image: "https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "LOW CODE / NO CODE DEVELOPMENT",
    description: "Customize CMS website using low/no-code tools like WordPress, Framer, WebFlow & Squarespace.",
    image: "https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "BLOCKCHAIN SOLUTIONS",
    description: "Implement secure, innovative blockchain technologies to enhance and empower your business operations.",
    image: "https://images.unsplash.com/photo-1639762681485-074b7f938ba0?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "AI SOLUTIONS & AUTOMATION",
    description: "Integrate advanced AI solutions to automate processes, and deliver personalized experiences.",
    image: "https://images.unsplash.com/photo-1677442136019-21780ecad995?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  }
]
</script>

<style scoped>
/* Additional hover effects if needed */
</style>