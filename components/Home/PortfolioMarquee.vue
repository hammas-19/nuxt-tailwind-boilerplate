<template>
  <section class="py-20 bg-white overflow-hidden">
          <div class="text-center mb-16">
        <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
          Our Portfolio
        </h2>
        <p class="text-lg text-gray-600">
          We provide services from tech to design.
        </p>
      </div>
    <div class="website-marquee">

      <!-- First Row - Left to Right -->
      <div class="marquee-row">
        <div class="marquee-track forward" v-for="n in 3" :key="'row1-' + n">
          <div v-for="(website, index) in websites.slice(0, 5)" :key="'site1-' + index + '-' + n" class="website-card">
            <img :src="website.image" :alt="website.name" class="website-image" />
          </div>
        </div>
      </div>

      <!-- Second Row - Right to Left -->
      <div class="marquee-row reverse">
        <div class="marquee-track backward" v-for="n in 3" :key="'row2-' + n">
          <div v-for="(website, index) in websites.slice(5)" :key="'site2-' + index + '-' + n" class="website-card">
            <img :src="website.image" :alt="website.name" class="website-image" />
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
const websites = [
  {
    name: 'E-commerce Platform',
    image: '/portfolio/1.jpg'
  },
  {
    name: 'SaaS Dashboard',
    image: '/portfolio/2.jpg'
  },
  {
    name: 'Tech Startup',
    image: '/portfolio/3.jpg'
  },
  {
    name: 'Healthcare App',
    image: '/portfolio/4.jpg'
  },
  {
    name: 'Financial Services',
    image: '/portfolio/5.jpg'
  },
  {
    name: 'Education Platform',
    image: '/portfolio/6.jpg'
  },
  {
    name: 'Travel Website',
    image: '/portfolio/7.jpg'
  },
  {
    name: 'Food Delivery',
    image: '/portfolio/8.jpg'
  },
  {
    name: 'Real Estate',
    image: '/portfolio/9.jpg'
  },
  {
    name: 'Real Estate',
    image: '/portfolio/10.jpg'
  }
]
</script>

<style scoped>
.website-marquee {
  position: relative;
  width: 100%;
  overflow: hidden;
}

.marquee-row {
  display: flex;
  align-items: center;
  overflow: hidden;
  margin-bottom: 2rem;
  white-space: nowrap;
}

.marquee-row.reverse {
  margin-bottom: 0;
}

.marquee-track {
  display: flex;
  align-items: center;
  gap: 3rem;
  flex-shrink: 0;
  animation-duration: 60s;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
}

.marquee-track.forward {
  animation-name: slideForward;
}

.marquee-track.backward {
  animation-name: slideBackward;
}

.website-card {
  flex-shrink: 0;
  width: 400px;
  height: 280px;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.website-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Forward animation (left to right) */
@keyframes slideForward {
  from {
    transform: translateX(0);
  }

  to {
    transform: translateX(-100%);
  }
}

/* Backward animation (right to left) */
@keyframes slideBackward {
  from {
    transform: translateX(-100%);
  }

  to {
    transform: translateX(0);
  }
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .website-card {
    width: 300px;
    height: 200px;
  }

  .marquee-track {
    gap: 2rem;
  }

  .marquee-row {
    margin-bottom: 1.5rem;
  }
}

@media (max-width: 480px) {
  .website-card {
    width: 250px;
    height: 180px;
  }

  .marquee-track {
    gap: 1.5rem;
  }
}
</style>