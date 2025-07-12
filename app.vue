<template>
  <div>
    <!-- In any component, button, or element -->
    <TheNavbar @open-modal="isModalOpen = true" />
    <HomeHero @open-modal="isModalOpen = true" />
    <HomeMarquee />
    <HomeOfferings />
    <HomeCTA1 @open-modal="isModalOpen = true" />
    <HomeServices />
    <HomeCTA2 @open-modal="isModalOpen = true" />
    <HomePortfolioMarquee />
    <HomeProcess />
    <HomeTestimonials />
    <HomeFaqs />
    <ContactModal :is-modal-open="isModalOpen" @close="isModalOpen = false" />
    <TheFooter />
  </div>
</template>
<script setup>
const isModalOpen = ref(false)
</script>
