<template>
  <section class="py-20 bg-white">
    <div class="def-container mx-auto px-4 sm:px-6 lg:px-8">

      <!-- Header -->
      <div class="text-center mb-16">
        <h2 class="text-4xl lg:text-5xl font-bold text-[#E2725B] mb-6">
          FAQs
        </h2>
        <p class="text-lg text-boss max-w-4xl mx-auto">
          Browse through common questions to get quick, clear answers and make informed decisions with confidence.
        </p>
      </div>

      <!-- FAQ Grid -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16 max-w-7xl mx-auto">

        <!-- Left Column FAQs -->
        <div class="space-y-0">
          <div v-for="(faq, index) in leftColumnFaqs" :key="'left-' + index"
            class="faq-item border-b border-gray-200 last:border-b-0">
            <!-- Question -->
            <button @click="toggleFaq('left', index)"
              class="w-full flex items-start gap-4 text-left py-6 transition-all duration-200">
              <!-- Plus/Minus Icon -->
              <div class="flex-shrink-0 mt-1">
                <div class="w-8 h-8 rounded-full border-2 flex items-center justify-center transition-all duration-300"
                  :class="faq.isOpen ? 'border-[#E2725B] bg-[#E2725B]' : 'border-peachy'">
                  <svg class="w-4 h-4 transition-all duration-300"
                    :class="faq.isOpen ? 'rotate-45 text-white' : 'text-peachy'" fill="none" stroke="currentColor"
                    viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M12 6v6m0 0v6m0-6h6m-6 0H6" />
                  </svg>
                </div>
              </div>

              <!-- Question Text -->
              <h3 class="text-lg font-medium text-gray-900 flex-1 text-left">
                {{ faq.question }}
              </h3>
            </button>

            <!-- Answer -->
            <div class="overflow-hidden transition-all duration-500 ease-in-out"
              :class="faq.isOpen ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'">
              <div class="ml-12 pb-6">
                <p class="text-gray-600 leading-relaxed">
                  {{ faq.answer }}
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- Right Column FAQs -->
        <div class="space-y-0">
          <div v-for="(faq, index) in rightColumnFaqs" :key="'right-' + index"
            class="faq-item border-b border-gray-200 last:border-b-0">
            <!-- Question -->
            <button @click="toggleFaq('right', index)"
              class="w-full flex items-start gap-4 text-left py-6 transition-all duration-200">
              <!-- Plus/Minus Icon -->
              <div class="flex-shrink-0 mt-1">
                <div class="w-8 h-8 rounded-full border-2 flex items-center justify-center transition-all duration-300"
                  :class="faq.isOpen ? 'border-[#E2725B] bg-[#E2725B]' : 'border-peachy'">
                  <svg class="w-4 h-4 transition-all duration-300"
                    :class="faq.isOpen ? 'rotate-45 text-white' : 'text-peachy'" fill="none" stroke="currentColor"
                    viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M12 6v6m0 0v6m0-6h6m-6 0H6" />
                  </svg>
                </div>
              </div>

              <!-- Question Text -->
              <h3 class="text-lg font-medium text-gray-900 flex-1 text-left">
                {{ faq.question }}
              </h3>
            </button>

            <!-- Answer -->
            <div class="overflow-hidden transition-all duration-500 ease-in-out"
              :class="faq.isOpen ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'">
              <div class="ml-12 pb-6">
                <p class="text-gray-600 leading-relaxed">
                  {{ faq.answer }}
                </p>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

// Left column FAQs
const leftColumnFaqs = ref([
  {
    question: "What is the best web development service for businesses?",
    answer: "We provide comprehensive web development services tailored to your business needs, including custom websites, e-commerce platforms, and web applications using the latest technologies and best practices.",
    isOpen: false
  },
  {
    question: "How do you ensure website quality?",
    answer: "We follow rigorous quality assurance processes including thorough testing, code reviews, performance optimization, and adherence to web standards to ensure your website meets the highest quality standards.",
    isOpen: false
  },
  {
    question: "Can I get 100% custom web design with Digi Ranchers?",
    answer: "Absolutely! We specialize in creating 100% custom web designs that reflect your brand identity and meet your specific business requirements. Every design is unique and tailored to your vision.",
    isOpen: false
  }
])

// Right column FAQs
const rightColumnFaqs = ref([
  {
    question: "Is it safe to hire a web development agency for businesses?",
    answer: "Hiring a professional web development agency is the safest choice for your business as there is no risk of project failure. Our team protects your data privacy and never shares details with anyone.",
    isOpen: true // This one starts open as shown in your image
  },
  {
    question: "What technologies or platforms do your web development services cover?",
    answer: "We work with a wide range of technologies including React, Vue.js, Node.js, Python, WordPress, Shopify, and many more. We choose the best technology stack based on your project requirements.",
    isOpen: false
  },
  {
    question: "How much does web development cost for businesses on a budget?",
    answer: "Our web development costs vary based on project complexity and requirements. We offer flexible pricing options and packages to accommodate different budgets while maintaining high quality standards.",
    isOpen: false
  }
])

// Toggle FAQ function
function toggleFaq(column, index) {
  if (column === 'left') {
    leftColumnFaqs.value[index].isOpen = !leftColumnFaqs.value[index].isOpen
  } else {
    rightColumnFaqs.value[index].isOpen = !rightColumnFaqs.value[index].isOpen
  }
}
</script>

<style scoped>
/* No additional styles needed */
</style>