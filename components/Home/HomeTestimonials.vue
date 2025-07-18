<template>
  <section class="py-20 bg-white">
    <div class="def-container mx-auto px-4 sm:px-6 lg:px-8">

      <!-- Header Section -->
      <div class="mb-16">
        <!-- Star Rating -->
        <div class="flex items-center gap-1 mb-6">
          <svg v-for="n in 5" :key="n" class="w-6 h-6 fill-[#E2725B]" viewBox="0 0 24 24">
            <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z" />
          </svg>
        </div>

        <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-6">
          What Our Clients Say.
        </h2>

        <p class="text-lg text-gray-600 max-w-2xl">
          Don't just take our word for it. We work day-in, day-out with a range of industries - each with unique
          development and digital marketing requirements. Here's what they have to say about the results:
        </p>
      </div>

      <!-- Testimonials Grid -->
      <div class="wrapper relative h-[600px] overflow-hidden">
        <!-- First Column -->
        <div class="marquee absolute left-0 w-1/3 md:pr-4">
          <div class="md:space-y-6 space-y-3">
            <div v-for="(item, index) in testimonials.slice(0, 4)" :key="'col1-' + index"
              class="bg-boss md:rounded-2xl rounded-lg md:p-6 p-3 shadow-lg">
              <!-- Star Rating -->
              <div class="flex items-center gap-1 mb-4">
                <svg v-for="n in 5" :key="n" class="w-4 h-4 fill-white" viewBox="0 0 24 24">
                  <path
                    d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z" />
                </svg>
              </div>

              <!-- Testimonial Content -->
              <blockquote class="text-white md:text-sm text-xs lg:text-base leading-relaxed md:mb-4 mb-2">
                "{{ item.comments }}"
              </blockquote>

              <!-- Author -->
              <div class="flex items-center justify-between">
                <div>
                  <div class="md:font-semibold font-medium md:text-base text-sm text-white">{{ item.name }}</div>
                  <div class="text-peachy text-sm">{{ item.city }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Second Column -->
        <div class="reverse absolute left-1/3 w-1/3 px-2">
          <div class="md:space-y-6 space-y-3">
            <div v-for="(item, index) in testimonials.slice(4, 7)" :key="'col2-' + index"
              class="bg-[#E2725B] md:rounded-2xl rounded-lg md:p-6 p-3 shadow-lg">
              <!-- Star Rating -->
              <div class="flex items-center gap-1 mb-4">
                <svg v-for="n in 5" :key="n" class="w-4 h-4 fill-white" viewBox="0 0 24 24">
                  <path
                    d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z" />
                </svg>
              </div>

              <!-- Testimonial Content -->
              <blockquote class="text-white md:text-sm text-xs lg:text-base leading-relaxed md:mb-4 mb-2">
                "{{ item.comments }}"
              </blockquote>

              <!-- Author -->
              <div class="flex items-center justify-between">
                <div>
                  <div class="md:font-semibold font-medium md:text-base text-sm text-white">{{ item.name }}</div>
                  <div class="text-boss text-sm">{{ item.city }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Third Column -->
        <div class="marquee-third absolute right-0 w-1/3 md:pl-4 ">
          <div class="md:space-y-6 space-y-3">
            <div v-for="(item, index) in testimonials.slice(7)" :key="'col3-' + index"
              class="bg-boss md:rounded-2xl rounded-lg md:p-6 p-3 shadow-lg">
              <!-- Star Rating -->
              <div class="flex items-center gap-1 mb-4">
                <svg v-for="n in 5" :key="n" class="w-4 h-4 fill-white" viewBox="0 0 24 24">
                  <path
                    d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z" />
                </svg>
              </div>

              <!-- Testimonial Content -->
              <blockquote class="text-white md:text-sm text-xs lg:text-base leading-relaxed md:mb-4 mb-2">
                "{{ item.comments }}"
              </blockquote>

              <!-- Author -->
              <div class="flex items-center justify-between">
                <div>
                  <div class="md:font-semibold font-medium md:text-base text-sm text-white">{{ item.name }}</div>
                  <div class="text-peachy text-sm">{{ item.city }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Gradient Overlays -->
        <!-- <div
          class="absolute top-0 left-0 w-full h-20 bg-gradient-to-b from-gray-50 to-transparent z-10 pointer-events-none">
        </div>
        <div
          class="absolute bottom-0 left-0 w-full h-20 bg-gradient-to-t from-gray-50 to-transparent z-10 pointer-events-none">
        </div> -->
      </div>

    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    name: 'Yawar Ali',
    city: 'Karachi',
    comments: 'This store exceeded my expectations. The quality is truly amazing!'
  },
  {
    name: 'Uzair Alam',
    city: 'Karachi',
    comments: 'A fantastic shopping experience from start to finish!'
  },
  {
    name: 'Fiza Fatima',
    city: 'Quetta',
    comments: 'Highly recommend this store to everyone. Great products and service!'
  },
  {
    name: 'Saad Adam',
    city: 'Hyderabad Sindh',
    comments: 'The team is outstanding, and the clothing is really impressive!'
  },
  {
    name: 'Kashaf Razzaq',
    city: 'Islamabad',
    comments: 'This store is an absolute game-changer for my wardrobe!'
  },
  {
    name: 'Hassan Tariq',
    city: 'Lahore',
    comments: "Top-quality clothing at affordable prices. Can't ask for more!"
  },
  {
    name: 'Areeba Khan',
    city: 'Peshawar',
    comments: 'The premium products here are worth every penny. Highly satisfied!'
  },
  {
    name: 'Zainab Siddiqui',
    city: 'Multan',
    comments: 'Affordable and trendy outfits. Perfect for every occasion!'
  },
  {
    name: 'Farhan Sheikh',
    city: 'Rawalpindi',
    comments: "Premium quality at a price that doesn't break the bank. Love it!"
  },
  {
    name: 'Mariam Ali',
    city: 'Faisalabad',
    comments: 'Stylish designs and great service. A perfect shopping destination!'
  }
]
</script>

<style scoped>
.marquee {
  animation: marqueescroll 15s linear infinite;
}

.reverse {
  animation: marqueescrollR 15s linear infinite;
}

.marquee-third {
  animation: marqueescroll 15s linear infinite;
}

@keyframes marqueescroll {
  0% {
    transform: translateY(0%);
  }

  100% {
    transform: translateY(-30%);
  }
}

@keyframes marqueescrollR {
  0% {
    transform: translateY(-30%);
  }

  100% {
    transform: translateY(0%);
  }
}
</style>