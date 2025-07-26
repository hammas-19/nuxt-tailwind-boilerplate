<template>
  <footer class="bg-peachy text-white py-16">
    <div class="def-container mx-auto px-4 sm:px-6 lg:px-8">

      <!-- Main Footer Content -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 lg:gap-12 mb-12">

        <!-- Company Info -->
        <div class="lg:col-span-1 flex justify-center flex-col items-center gap-4">
          <img src="/techLabsLogo.png" class="max-w-40 w-fit" alt="techLabsLogo">
          <p class="text-white/80 text-lg">
            Creative Design & Marketing
          </p>
        </div>

        <!-- Navigation Links -->
        <div>
          <h3 class="text-lg font-semibold text-white mb-6">Navigation</h3>
          <ul class="space-y-3">
            <li>
              <a href="/#portfolio" class="text-white/80 hover:text-white transition-colors duration-200">
                Work
              </a>
            </li>
            <li>
              <a href="/#aboutus" class="text-white/80 hover:text-white transition-colors duration-200">
                About Us
              </a>
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
              <a href="/#services" class="text-white/80 hover:text-white transition-colors duration-200">
                Animation
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
      <div class="border-t border-white/20 pt-8">
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
            <a href="#" class="text-white/80 hover:text-white transition-colors duration-200">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path
                  d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z" />
              </svg>
            </a>

            <a href="#" class="text-white/80 hover:text-white transition-colors duration-200">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path
                  d="M12.017 0C5.396 0 .029 5.367.029 11.987c0 5.079 3.158 9.417 7.618 11.174-.105-.949-.199-2.403.041-3.439.219-.937 1.406-5.957 1.406-5.957s-.359-.72-.359-1.781c0-1.663.967-2.911 2.168-2.911 1.024 0 1.518.769 1.518 1.688 0 1.029-.653 2.567-.992 3.992-.285 1.193.6 2.165 1.775 2.165 2.128 0 3.768-2.245 3.768-5.487 0-2.861-2.063-4.869-5.008-4.869-3.41 0-5.409 2.562-5.409 5.199 0 1.033.394 2.143.889 2.741.099.12.112.225.085.345-.09.375-.293 1.199-.334 1.363-.053.225-.172.271-.402.165-1.495-.69-2.433-2.878-2.433-4.646 0-3.776 2.748-7.252 7.92-7.252 4.158 0 7.392 2.967 7.392 6.923 0 4.135-2.607 7.462-6.233 7.462-1.214 0-2.357-.629-2.746-1.378l-.747 2.848c-.269 1.045-1.004 2.352-1.498 3.146 1.123.345 2.306.535 3.55.535 6.624 0 11.99-5.367 11.99-11.987C24.007 5.367 18.641.001 12.017.001z" />
              </svg>
            </a>

            <a href="#" class="text-white/80 hover:text-white transition-colors duration-200">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path
                  d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z" />
              </svg>
            </a>

            <a href="#" class="text-white/80 hover:text-white transition-colors duration-200">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path
                  d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z" />
              </svg>
            </a>

            <a href="#" class="text-white/80 hover:text-white transition-colors duration-200">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path
                  d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z" />
              </svg>
            </a>
          </div>

        </div>

        <!-- Copyright -->
        <div class="mt-8 pt-6 border-t border-white/20">
          <p class="text-sm text-white/80 text-center lg:text-left">
            © Copyright 2025. All rights reserved by Mr TechLabs
          </p>
        </div>

      </div>
    </div>
  </footer>
</template>
