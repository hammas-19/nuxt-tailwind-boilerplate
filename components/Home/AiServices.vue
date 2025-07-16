<template>
  <section class="pb-20 bg-white">
    <div class="def-container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="mb-16 w-full max-w-3xl">
        <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
          AI SERVICES
        </h2>
        <p class="text-lg text-gray-600">
          Our AI services utilize advanced technology to create customized solutions that are easy for you to use.
          We help clients every step of the way with workshops, showing them how to design, set up, and easily add
          these solutions to their business.
        </p>
      </div>
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-20">

        <!-- Left Side - Service Cards -->
        <div class="space-y-6">
          <div v-for="(service, index) in services" :key="service.id"
            class="bg-boss rounded-2xl p-8 text-white relative overflow-hidden group hover:transform hover:scale-105 transition-all duration-300">
            <!-- Number Badge -->
            <div class="text-[#E2725B] font-bold text-lg mb-4">
              {{ String(index + 1).padStart(2, '0') }}
            </div>

            <!-- Service Title -->
            <h3 class="text-3xl font-bold mb-4">{{ service.title }}</h3>

            <!-- Service Description -->
            <p class="text-gray-300 text-lg leading-relaxed mb-6">
              {{ service.description }}
            </p>

            <!-- Icon -->
            <div class="absolute top-8 right-8">
              <Icon :name="service.icon" class="min-h-8 min-w-8 text-white" />
            </div>
          </div>
        </div>

        <!-- Right Side - Sticky Content -->
        <div
          class="lg:sticky lg:top-32 lg:self-start max-w-lg  flex justify-center items-center overflow-hidden flex-col">

          <img src="/AI/secImage.png" class="object-cover bg-peachy h-full w-full md:rounded-4xl rounded-2xl" alt="">
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

// Services data array
const services = ref([
  {
    id: 1,
    title: 'SPECIALIZED AI-POWERED TOOLS & PLATFORMS:',
    description: 'Providing tools that use AI to uncover deeper insights from business data, beyond traditional dashboards.',
    icon: 'hugeicons:artificial-intelligence-04'
  },
  {
    id: 2,
    title: 'AI MAINTENANCE & OPTIMIZATION:',
    description: 'Ensuring deployed AI models continue to perform accurately over time and retraining them with new data as needed.',
    icon: 'hugeicons:artificial-intelligence-03'
  },
  {
    id: 3,
    title: 'NATURAL LANGUAGE PROCESSING (NLP) & UNDERSTANDING (NLU):',
    description: 'Developing AI that can understand, interpret, and generate human language',
    icon: 'healthicons:artificial-intelligence-outline'
  },
  {
    id: 2,
    title: 'COMPUTER VISION DEVELOPMENT',
    description: 'Building AI that can "see" and interpret images and videos',
    icon: 'hugeicons:artificial-intelligence-03'
  },
  {
    id: 3,
    title: 'AI INTEGRATION & IMPLEMENTATION',
    description: 'Connecting existing software and systems with ready-made AI services',
    icon: 'streamline:artificial-intelligence-spark'
  },
  {
    id: 2,
    title: 'AI DEVELOPMENT & CUSTOM SOLUTIONS',
    description: 'Building unique AI models from scratch tailored to your specific business problem.',
    icon: 'hugeicons:artificial-intelligence-03'
  },
  {
    id: 3,
    title: 'AI STRATEGY & CONSULTING',
    description: 'We help you understand if AI is right for your business, what data you have, and where AI can help you most.',
    icon: 'streamline:artificial-intelligence-spark'
  },
  {
    id: 3,
    title: 'AI CHATBOT INTEGRATION',
    description: 'Add smart chatbots to automate support and engage customers 24/7.',
    icon: 'hugeicons:machine-robot'
  },
  {
    id: 4,
    title: 'AI-POWERED DATA ANALYTICS',
    description: 'We use AI to find key trends in your data, helping you make smarter business choices.',
    icon: 'hugeicons:robot-01'
  }
])
</script>

<style scoped>
/* Custom scrolling behavior for sticky positioning */
@media (min-width: 1024px) {
  .lg\:sticky {
    position: sticky;
  }
}
</style>