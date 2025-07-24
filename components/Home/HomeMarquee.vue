<template>
  <div class="marquee_container text-7xl font-sans text-white font-bold uppercase">
    <div class="marquee">
      <!-- <span class="pr-10"></span> -->
      <h2>We Make it</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Simple to</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Grow Your Business.</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>We Make it</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Simple to</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Grow Your Business.</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>We Make it</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Simple to</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Grow Your Business.</h2>
    </div>
    <div class="marquee">
      <!-- <span class="pr-10"></span> -->
      <h2>We Make it</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Simple to</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Grow Your Business.</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>We Make it</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Simple to</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Grow Your Business.</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>We Make it</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Simple to</h2>
      <!-- <span class="pr-10"></span> -->
      <h2>Grow Your Business.</h2>
    </div>
  </div>
</template>
<style scoped>

.marquee_container {
  width: 100%;
  overflow: hidden;
  white-space: nowrap;
  background: #E2725B;
  padding: 0.2rem 0;
}

.marquee {
  display: inline-block;
  animation: marquee 30s linear infinite;
}

@keyframes marquee {
  from {
    transform: translate3d(0, 0, 0);
  }

  to {
    transform: translate3d(-100%, 0, 0);
  }
}

h2 {
  display: inline-block;
  margin-right: 50px;
}
</style>