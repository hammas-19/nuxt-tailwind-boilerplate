<template>
  <div>
    <!-- In any component, button, or element -->
    <TheNavbar @open-modal="isModalOpen = true" />
    <div id="home">
      <HomeHero @open-modal="isModalOpen = true" />
    </div>
    <HomeMarquee />
    <div id="aboutus">
      <HomeOfferings />
    </div>
    <HomeCTA1 @open-modal="isModalOpen = true" />
    <div id="services">
      <HomeServices />
    </div>
    <HomeAiServices />
    <HomeCTA2 @open-modal="isModalOpen = true" />
    <div id="portfolio">
      <HomePortfolioMarquee />
    </div>
    <HomeProcess />
    <div id="testimonials">
      <HomeTestimonials />
    </div>
    <HomeFaqs />
    <HomeLocations @open-modal="isModalOpen = true" />
    <ContactModal :is-modal-open="isModalOpen" @close="isModalOpen = false" />
    <TheFooter @open-modal="isModalOpen = true" />
  </div>
</template>
<script setup>
const isModalOpen = ref(false)
</script>
