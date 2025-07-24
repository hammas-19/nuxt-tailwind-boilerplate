<template>
  <section class="py-20 bg-white">
    <div class=" mx-auto px-4 sm:px-6 lg:px-8">

      <!-- Header -->
      <div class="text-center mb-16">
        <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
          GROWTH DRIVEN BY ACTION
        </h2>
        <p class="text-lg text-gray-600">
          For business growth through execution, we offer everything you need. Our services span creative, digital, and
          IT, ensuring total satisfaction for all our clients.
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
              <div class="md:gap-10 gap-4 flex flex-wrap items-center">
                <h3
                  class="text-2xl lg:text-3xl text-gray-900 group-hover:text-white mb-3 transition-colors duration-500 w-[350px]">
                  {{ service.title }}
                </h3>
                <p
                  class="text-gray-600 group-hover:text-white/90 text-base lg:text-lg transition-colors duration-500 w-fit ">
                  {{ service.description }}
                </p>
              </div>

            </div>

            <!-- Arrow Icon -->
            <div class="flex-shrink-0 ml-6">
              <div
                class="w-12 h-12 flex items-center justify-center bg-gray-100 group-hover:bg-white/20 rounded-full transition-all duration-500">
                <svg class="w-6 h-6 text-gray-600 !group-hover:text-white transition-colors duration-500"
                  xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24">
                  <path d="M5 17.59L15.59 7H9V5h10v10h-2V8.41L6.41 19z" />
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
    title: "WORDPRESS",
    description: "Build and manage powerful WordPress websites.",
    image: "/services/Wordpress.png"
  },
  {
    title: "E-COMMERCE",
    description: "Set up and optimize online stores for sales.",
    image: "/services/eCommerce.png"
  },
  {
    title: "SHOPIFY",
    description: "Design and launch high-converting Shopify stores.",
    image: "/services/Shopify.png"
  },
  {
    title: "CONTENT WRITING",
    description: "Create words that grab attention and get results.",
    image: "https://images.unsplash.com/photo-1455390582262-044cdead277a?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "SOCIAL MEDIA MANAGEMENT",
    description: "Handle social media to engage audiences and build brands.",
    image: "https://images.unsplash.com/photo-1611162617474-5b21e879e113?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "SOCIAL MEDIA ADVERTISING",
    description: "Create targeted social media ads that drive results.",
    image: "/services/SocialMedia.jpg"
  },
  {
    title: "INFLUENCER MARKETING",
    description: "Get your brand seen and trusted through influential people.",
    image: "/services/InfluencerMarketing.jpg"
  },
  {
    title: "GRAPHIC DESIGN",
    description: "Craft stunning visuals that make brands stand out.",
    image: "https://images.unsplash.com/photo-1561070791-2526d30994b5?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "APP DEVELOPMENT",
    description: "Build custom mobile apps tailored to business needs.",
    image: "https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "BRANDING",
    description: "Create strong, memorable brand identities.",
    image: "https://images.unsplash.com/photo-1553835973-dec43bfddbeb?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "ANIMATION",
    description: "Bring ideas to life with captivating animation.",
    image: "https://images.unsplash.com/photo-1509343256512-d77a5cb3791b?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "OUTSOURCED ACCOUNTING & HR",
    description: "Let us handle your accounting and HR so you can focus on your business.",
    image: "https://images.unsplash.com/photo-1554224155-6726b3ff858f?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  },
  {
    title: "ERP DEVELOPMENT & IMPLEMENTATION",
    description: "We build and set up powerful software to help you run your entire business smoothly.",
    image: "https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&w=150&h=150&fit=crop&crop=center"
  }
]
</script>

<style scoped>
/* Additional hover effects if needed */
</style>