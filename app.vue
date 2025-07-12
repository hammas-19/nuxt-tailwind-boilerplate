<template>
  <div>
    <!-- In any component, button, or element -->
    <TheNavbar />
    <HomeHero />
    <HomeMarquee />
    <HomeOfferings />
    <HomeCTA1 />
    <HomeServices />
    <HomeCTA2 />
    <HomePortfolioMarquee />
    <HomeProcess />
    <HomeTestimonials />
    <HomeFaqs />
    <ContactModal :isModalOpen="isModalOpen" @close="isModalOpen = false" />
    <TheFooter />
  </div>
</template>
<script setup>
const isModalOpen = ref(true)
</script>
