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
        <!-- First Column - Pakistan -->
        <div class="marquee absolute left-0 w-1/3 md:pr-4">
          <div class="md:space-y-6 space-y-3">
            <div v-for="(item, index) in pakistanTestimonials" :key="'pak-' + index"
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
                  <div class="text-peachy text-sm">{{ item.country }}</div>
                </div>
              </div>
            </div>
            <div v-for="(item, index) in pakistanTestimonials" :key="'pak-' + index"
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
                  <div class="text-peachy text-sm">{{ item.country }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Second Column - UAE -->
        <div class="reverse absolute left-1/3 w-1/3 px-2">
          <div class="md:space-y-6 space-y-3">
            <div v-for="(item, index) in uaeTestimonials" :key="'uae-' + index"
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
                  <div class="text-boss text-sm">{{ item.country }}</div>
                </div>
              </div>
            </div>
            <div v-for="(item, index) in uaeTestimonials" :key="'uae-' + index"
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
                  <div class="text-boss text-sm">{{ item.country }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Third Column - USA -->
        <div class="marquee-third absolute right-0 w-1/3 md:pl-4 ">
          <div class="md:space-y-6 space-y-3">
            <div v-for="(item, index) in usaTestimonials" :key="'usa-' + index"
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
                  <div class="text-peachy text-sm">{{ item.country }}</div>
                </div>
              </div>
            </div>
            <div v-for="(item, index) in usaTestimonials" :key="'usa-' + index"
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
                  <div class="text-peachy text-sm">{{ item.country }}</div>
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
const pakistanTestimonials = [
  {
    name: 'Ali Raza',
    country: 'Pakistan',
    comments: 'Great service and communication. Mr Tech Labs helped grow our online presence in just 3 months!'
  },
  {
    name: 'Mehwish Javed',
    country: 'Pakistan',
    comments: 'They revamped our entire digital strategy. Sales are up and the branding looks amazing.'
  },
  {
    name: 'Usman Tariq',
    country: 'Pakistan',
    comments: 'Highly professional team. They really understand the local market and trends.'
  },
  {
    name: 'Rabia Khan',
    country: 'Pakistan',
    comments: 'We saw noticeable improvement in leads after their SEO and ad campaigns.'
  },
  {
    name: 'Hamza Aslam',
    country: 'Pakistan',
    comments: 'Mr Tech Labs is now our go-to for all marketing needs. Very responsive team.'
  },
  {
    name: 'Fatima Noor',
    country: 'Pakistan',
    comments: 'Excellent results with Google Ads and social media. Highly recommend for SMEs in Pakistan.'
  }
]

const uaeTestimonials = [
  {
    name: 'Omar Al Mansoori',
    country: 'UAE',
    comments: 'Impressed by their deep understanding of digital growth in the Gulf market.'
  },
  {
    name: 'Layla Farooq',
    country: 'UAE',
    comments: 'The campaigns they ran for our salon chain got great traction. Worth every dirham.'
  },
  {
    name: 'Ahmed Nasser',
    country: 'UAE',
    comments: 'Very professional. Delivered ahead of deadlines and exceeded expectations.'
  },
  {
    name: 'Reem Khalid',
    country: 'UAE',
    comments: 'Loved their branding ideas! Mr Tech Labs gave our company a fresh and modern look.'
  },
  {
    name: 'Tariq Sultan',
    country: 'UAE',
    comments: 'Their team worked seamlessly with ours. Results were visible in the first month.'
  },
  {
    name: 'Zahra Mehmood',
    country: 'UAE',
    comments: 'From web development to digital ads, they managed everything flawlessly.'
  }
]

const usaTestimonials = [
  {
    name: 'Jason Miller',
    country: 'USA',
    comments: 'Finding Mr Tech Labs was a game changer for our ecommerce business.'
  },
  {
    name: 'Sophia Garcia',
    country: 'USA',
    comments: 'They really know how to scale businesses online. Great value and strategy.'
  },
  {
    name: 'Mark Thompson',
    country: 'USA',
    comments: 'Efficient, creative, and results-driven. They helped boost our conversions significantly.'
  },
  {
    name: 'Emily Johnson',
    country: 'USA',
    comments: 'Super professional team with fast turnarounds. Loved their work on our ad creatives.'
  },
  {
    name: 'Aiden Brooks',
    country: 'USA',
    comments: 'Weve worked with several agencies, but Mr Tech Labs delivered real ROI.'
  },
  {
    name: 'Rachel Lee',
    country: 'USA',
    comments: 'SEO, paid ads, email marketing—they handled it all with impressive results.'
  }
]
</script>

<style scoped>
.marquee {
  animation: marqueescroll 45s linear infinite;
}

.reverse {
  animation: marqueescrollR 45s linear infinite;
}

.marquee-third {
  animation: marqueescroll 45s linear infinite;
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