<template>
  <section class="py-12 sm:py-16 md:py-20 bg-white">
    <div class="def-container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 sm:gap-12 lg:gap-20">

        <!-- Left Side - Sticky Content -->
        <div class="lg:sticky lg:top-32 lg:self-start">
          <div class="max-w-lg">
            <!-- About Badge -->
            <div class="inline-block text-[#E2725B] font-semibold text-lg mb-4">
              About us
            </div>

            <!-- Main Heading -->
            <h2 class="text-2xl sm:text-3xl md:text-4xl lg:text-5xl font-bold text-boss mb-6 leading-tight">
              EXCLUSIVE PARTNERSHIPS: YOUR COMPETITIVE FUTURE
            </h2>

            <!-- Description -->
            <p class="text-base sm:text-lg text-gray-600 leading-relaxed mb-8">
              We hold strong negotiation power with our partners, granting you exclusive access to the latest media
              products, unique collaborations, and inside insights. This ensures you outpace your competition.
            </p>

            <!-- Team Members -->
            <div class="space-y-4 sm:space-y-6">
              <h3 class="text-xl sm:text-2xl font-bold text-boss mb-4">Meet Our Team</h3>
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 sm:gap-6">
                <div v-for="member in teamMembers" :key="member.id"
                  class="bg-boss rounded-2xl p-4 sm:p-6 shadow-lg hover:shadow-xl transition-all duration-300 hover:transform hover:scale-105">
                  <!-- Member Image -->
                  <div class="relative mb-4">
                    <img :src="member.image" :alt="member.name"
                      class="w-16 h-16 sm:w-20 sm:h-20 rounded-full object-cover mx-auto border-4 border-[#E2725B]" />
                  </div>

                  <!-- Member Info -->
                  <div class="text-center">
                    <h4 class="font-bold text-white text-lg sm:text-xl mb-1">{{ member.name }}</h4>
                    <p class="text-[#E2725B] font-semibold text-sm sm:text-base mb-2">{{ member.position }}</p>
                    <p class="text-gray-300 text-xs sm:text-sm leading-relaxed">{{ member.description }}</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Right Side - Cards -->
        <div class="space-y-4 sm:space-y-6">
          <div v-for="(item, index) in aboutData" :key="item.id"
            class="bg-boss rounded-xl sm:rounded-2xl p-6 sm:p-8 text-white relative overflow-hidden group hover:transform hover:scale-105 transition-all duration-300">
            <!-- Service Title -->
            <h3 class="text-2xl sm:text-3xl font-bold mb-4 pr-12">{{ item.title }}</h3>

            <!-- Service Description -->
            <div class="text-gray-300 text-base sm:text-lg leading-relaxed mb-6">
              <div v-if="item.type === 'values'">
                <div v-for="value in item.values" :key="value.name" class="mb-3 sm:mb-4">
                  <div class="font-semibold text-white mb-1 text-sm sm:text-base">{{ value.name }}:</div>
                  <div class="text-sm sm:text-base">{{ value.description }}</div>
                </div>
              </div>
              <p v-else class="text-sm sm:text-base">{{ item.description }}</p>
            </div>

            <!-- Icon -->
            <div class="absolute top-6 sm:top-8 right-6 sm:right-8">
              <Icon :name="item.icon" class="min-h-6 min-w-6 sm:min-h-8 sm:min-w-8 text-white" />
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

// About us data array
const aboutData = ref([
  {
    id: 1,
    type: 'values',
    title: 'OUR VALUES',
    icon: 'hugeicons:vision',
    values: [
      {
        name: 'Results Driven',
        description: 'We focus on delivering real outcomes.'
      },
      {
        name: 'Always Learning',
        description: 'We\'re constantly improving and adapting.'
      },
      {
        name: 'One Team, One Goal',
        description: 'We achieve together.'
      },
      {
        name: 'Simple Solutions',
        description: 'We believe in making things easy to understand and use.'
      },
      {
        name: 'Client First',
        description: 'Your success is our top priority.'
      }
    ]
  },
  {
    id: 2,
    type: 'mission',
    title: 'OUR MISSION',
    description: 'To supercharge the growth of our clients businesses.',
    icon: 'hugeicons:target-01'
  },
  {
    id: 3,
    type: 'vision',
    title: 'OUR VISION',
    description: 'To be the best and most sought-after performance marketing company in the world.',
    icon: 'hugeicons:eye'
  }
])

// Team members data
const teamMembers = ref([
  {
    id: 1,
    name: 'Sarah Johnson',
    position: 'CEO & Founder',
    description: 'Visionary leader with 15+ years in digital marketing and business strategy.',
    image: '/Team/CEO.jpeg'
  },
  {
    id: 2,
    name: 'Michael Chen',
    position: 'Project Manager',
    description: 'Expert in project coordination and team leadership, ensuring seamless execution.',
    image: '/Team/ProjectManager.jpeg'
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