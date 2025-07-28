<template>
  <footer class="bg-peachy text-white pt-16 pb-5">
    <div class="def-container mx-auto px-4 sm:px-6 lg:px-8">

      <!-- Main Footer Content -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 lg:gap-12 mb-12">

        <!-- Company Info -->
        <div class="lg:col-span-1 flex justify-center flex-col items-center gap-4">
          <a href="/">
            <img src="/techLabsLogo.png" class="max-w-40 w-fit" alt="techLabsLogo">
          </a>
            <p class="text-white/80 text-lg">
            Creative Design & Marketing
          </p>
        </div>

        <!-- Navigation Links -->
        <div>
          <h3 class="text-lg font-semibold text-white mb-6">Navigation</h3>
          <ul class="space-y-3">
            <li>
              <a href="/" class="text-white/80 hover:text-white transition-colors duration-200">
                Home
              </a>
            </li>
            <li>
              <a href="/#aboutus" class="text-white/80 hover:text-white transition-colors duration-200">
                About Us
              </a>
            </li>
            <li>
              <a href="/#services" class="text-white/80 hover:text-white transition-colors duration-200">
                Services
              </a>
            </li>
            <li>
              <a href="/#portfolio" class="text-white/80 hover:text-white transition-colors duration-200">
                Portfolio
              </a>
            </li>
            <li>
              <button @click="$emit('openModal')" class="cursor-pointer text-white/80 hover:text-white transition-colors duration-200">
                Contact Us
              </button>
            </li>
            <!-- <li>
              <NuxtLink to="/news" class="text-white/80 hover:text-white transition-colors duration-200">
                News
              </NuxtLink>
            </li> -->
            <!-- <li>
              <button to="/contact" class="text-white/80 hover:text-white transition-colors duration-200">
                Contact
              </button>
            </li> -->
            <!-- <li>
              <NuxtLink to="/careers" class="text-white/80 hover:text-white transition-colors duration-200">
                Current Opportunities
              </NuxtLink>
            </li> -->
          </ul>
        </div>

        <!-- Services -->
        <div>
          <h3 class="text-lg font-semibold text-white mb-6">What we do</h3>
          <ul class="space-y-3">
            <li>
              <a href="/#services" class="text-white/80 hover:text-white transition-colors duration-200">
                Branding
              </a>
            </li>
            <li>
              <a href="/#services" class="text-white/80 hover:text-white transition-colors duration-200">
                Digital Marketing
              </a>
            </li>
            <li>
              <a href="/#services" class="text-white/80 hover:text-white transition-colors duration-200">
                Web Design
              </a>
            </li>
            <li>
              <a href="/#services" class="text-white/80 hover:text-white transition-colors duration-200">
                Development
              </a>
            </li>
            <li>
              <a href="/#services" class="text-white hover:text-white/80 transition-colors duration-200">
                Graphic Design
              </a>
            </li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div>
          <h3 class="text-lg font-semibold text-white mb-6">Mr TechLabs</h3>
          <div class="space-y-3 text-white/80">
            <p>
              Office: Off2-0109 <br> Ras Al Khor <br> Industrial Area 3 <br> Dubai
            </p>

            <div class="pt-4">
              <p class="text-white font-medium mb-2">+971 58 1237912</p>
              <a href="mailto:official.mrtechlabs@gmail.com"
                class="text-white hover:text-white/80 transition-colors duration-200">
                official.mrtechlabs@gmail.com
              </a>
            </div>
          </div>
        </div>

      </div>

      <!-- Footer Bottom -->
      <div class="border-t border-white/20 pt-3">
        <div class="flex flex-col lg:flex-row justify-between items-center gap-6">

          <!-- Legal Links -->
          <div class="flex flex-wrap items-center gap-6 text-sm text-white/80">
            <NuxtLink to="/terms" class="hover:text-white transition-colors duration-200">
              Terms & conditions
            </NuxtLink>
            <span class="text-white/50">|</span>
            <NuxtLink to="/privacy" class="hover:text-white transition-colors duration-200">
              Privacy policy
            </NuxtLink>
            <span class="text-white/50">|</span>
            <!-- <NuxtLink to="/join" class="hover:text-white transition-colors duration-200">
              Join us
            </NuxtLink> -->
          </div>

          <!-- Social Media Icons -->
          <div class="flex items-center gap-4">
            <a href="https://www.instagram.com/mr.techlabs?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw=="
              target="_blank" class="text-white/80 hover:text-white transition-colors duration-200">
              <Icon name="uil:instagram" class="min-h-10 min-w-10 text-white" />
            </a>
            <a href="https://www.linkedin.com/company/mrtechlabs" target="_blank"
              class="text-white/80 hover:text-white transition-colors duration-200">
              <Icon name="tabler:brand-linkedin" class="min-h-10 min-w-10 text-white" />
            </a>
          </div>

        </div>

        <!-- Copyright -->
        <div class="mt-3 pt-3 border-t border-white/20">
          <p class="text-sm text-white/80 text-center lg:text-left">
            © Copyright 2025. All rights reserved by Mr TechLabs
          </p>
        </div>

      </div>
    </div>
  </footer>
</template>
