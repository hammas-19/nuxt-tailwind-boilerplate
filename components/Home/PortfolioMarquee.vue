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
    image: 'https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?w=800&h=600&fit=crop&crop=center'
  },
  {
    name: 'SaaS Dashboard',
    image: 'https://images.unsplash.com/photo-1551650975-87deedd944c3?w=800&h=600&fit=crop&crop=center'
  },
  {
    name: 'Tech Startup',
    image: 'https://images.unsplash.com/photo-1460925895917-afdab827c52f?w=800&h=600&fit=crop&crop=center'
  },
  {
    name: 'Healthcare App',
    image: 'https://images.unsplash.com/photo-1576091160399-112ba8d25d1f?w=800&h=600&fit=crop&crop=center'
  },
  {
    name: 'Financial Services',
    image: 'https://images.unsplash.com/photo-1563013544-824ae1b704d3?w=800&h=600&fit=crop&crop=center'
  },
  {
    name: 'Education Platform',
    image: 'https://images.unsplash.com/photo-1522202176988-66273c2fd55f?w=800&h=600&fit=crop&crop=center'
  },
  {
    name: 'Travel Website',
    image: 'https://images.unsplash.com/photo-1469474968028-56623f02e42e?w=800&h=600&fit=crop&crop=center'
  },
  {
    name: 'Food Delivery',
    image: 'https://images.unsplash.com/photo-1504674900247-0877df9cc836?w=800&h=600&fit=crop&crop=center'
  },
  {
    name: 'Real Estate',
    image: 'https://images.unsplash.com/photo-1560518883-ce09059eeffa?w=800&h=600&fit=crop&crop=center'
  },
  {
    name: 'Fitness App',
    image: 'https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=800&h=600&fit=crop&crop=center'
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