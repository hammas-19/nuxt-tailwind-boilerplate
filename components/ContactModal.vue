<!-- ContactModal.vue -->
<template>
  <!-- Modal Overlay -->
  <div v-if="props.isModalOpen"
    class="fixed inset-0 z-50 flex items-center justify-center bg-[#ffffff3a] backdrop-blur-2xl bg-opacity-60 p-4"
    @click="closeModal">
    <!-- Success Message -->
    <div v-if="showSuccess"
      class="bg-white rounded-3xl shadow-2xl max-w-md w-full p-8 text-center transform transition-all duration-500"
      @click.stop>
      <div class="w-20 h-20 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-6">
        <svg class="w-10 h-10 text-green-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
        </svg>
      </div>
      <h3 class="text-2xl font-bold text-gray-800 mb-3">Thank You! 🎉</h3>
      <p class="text-gray-600 mb-6">
        We've received your message and will contact you within 24 hours to discuss your project.
      </p>
      <button @click="closeModal"
        class="bg-[#E2725B] hover:bg-[#d65a42] text-white font-semibold py-3 px-8 rounded-xl transition-colors">
        Close
      </button>
    </div>

    <!-- Error Message -->
    <div v-else-if="showError"
      class="bg-white rounded-3xl shadow-2xl max-w-md w-full p-8 text-center transform transition-all duration-500"
      @click.stop>
      <div class="w-20 h-20 bg-red-100 rounded-full flex items-center justify-center mx-auto mb-6">
        <svg class="w-10 h-10 text-red-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-2.5L13.732 4c-.77-.833-1.964-.833-2.732 0L3.732 16.5c-.77.833.192 2.5 1.732 2.5z" />
        </svg>
      </div>
      <h3 class="text-2xl font-bold text-gray-800 mb-3">Oops! Something went wrong</h3>
      <p class="text-gray-600 mb-6">
        There was an error sending your message. Please try again.
      </p>
      <button @click="showError = false"
        class="bg-[#E2725B] hover:bg-[#d65a42] text-white font-semibold py-3 px-8 rounded-xl transition-colors">
        Try Again
      </button>
    </div>

    <!-- Main Modal Content -->
    <div v-else @click.stop
      class="bg-white rounded-2xl shadow-2xl max-w-3xl w-full max-h-[90vh] overflow-y-auto relative">

      <!-- Header -->
      <div class="bg-gradient-to-r from-[#E2725B] to-[#d65a42] px-6 py-5 text-white rounded-t-2xl">
        <div class="flex justify-between items-center">
          <div>
            <h2 class="text-2xl font-bold">Have a project in mind ? ✨</h2>
            <p class="text-white/90">Share your information below and we'll connect with you within 24 hours.</p>
          </div>
          <button @click="closeModal" class="p-2 hover:bg-white/20 rounded-full transition-all duration-200">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Form Content -->
      <div class="p-6">

        <!-- Progress Bar -->
        <div class="mb-6">
          <div class="flex justify-between text-sm text-gray-600 mb-2">
            <span>Progress</span>
            <span>{{ completionPercentage }}%</span>
          </div>
          <div class="w-full bg-gray-200 rounded-full h-2">
            <div class="bg-gradient-to-r from-[#E2725B] to-[#d65a42] h-2 rounded-full transition-all duration-500"
              :style="{ width: completionPercentage + '%' }"></div>
          </div>
        </div>

        <!-- Form -->
        <form @submit.prevent="submitForm" class="space-y-4">

          <!-- Personal Info -->
          <div class="grid grid-cols-1 lg:grid-cols-2 gap-4">
            <!-- First Name -->
            <div>
              <label class="block text-gray-700 font-medium mb-2 text-sm">
                First Name <span class="text-[#E2725B]">*</span>
              </label>
              <div class="relative">
                <input v-model="form.firstName" name="first_name" type="text" required
                  class="w-full px-4 py-3 border-2 border-gray-200 rounded-lg focus:border-[#E2725B] transition-all duration-300"
                  placeholder="John" :class="{ 'border-[#E2725B]': form.firstName }" />
                <svg v-if="form.firstName" class="absolute right-3 top-3.5 w-4 h-4 text-green-500" fill="currentColor"
                  viewBox="0 0 20 20">
                  <path fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd" />
                </svg>
              </div>
            </div>

            <!-- Contact Number -->
            <div>
              <label class="block text-gray-700 font-medium mb-2 text-sm">
                Contact Number <span class="text-[#E2725B]">*</span>
              </label>
              <div class="relative">
                <input v-model="form.contactNumber" name="phone" type="tel" required
                  class="w-full px-4 py-3 border-2 border-gray-200 rounded-lg focus:border-[#E2725B] transition-all duration-300"
                  placeholder="+1 (555) 123-4567" :class="{ 'border-[#E2725B]': form.contactNumber }" />
                <svg v-if="form.contactNumber" class="absolute right-3 top-3.5 w-4 h-4 text-green-500"
                  fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd" />
                </svg>
              </div>
            </div>
          </div>

          <div class="grid grid-cols-1 lg:grid-cols-2 gap-4">
            <!-- Email Address -->
            <div>
              <label class="block text-gray-700 font-medium mb-2 text-sm">
                Email Address <span class="text-[#E2725B]">*</span>
              </label>
              <div class="relative">
                <input v-model="form.email" name="email" type="email" required
                  class="w-full px-4 py-3 border-2 border-gray-200 rounded-lg focus:border-[#E2725B] transition-all duration-300"
                  placeholder="john@company.com" :class="{ 'border-[#E2725B]': form.email }" />
                <svg v-if="form.email && isValidEmail" class="absolute right-3 top-3.5 w-4 h-4 text-green-500"
                  fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd" />
                </svg>
              </div>
            </div>

            <!-- Company Website -->
            <div>
              <label class="block text-gray-700 font-medium mb-2 text-sm">
                Company Website
              </label>
              <div class="relative">
                <input v-model="form.website" name="website" type="url"
                  class="w-full px-4 py-3 border-2 border-gray-200 rounded-lg focus:border-[#E2725B] transition-all duration-300"
                  placeholder="https://yourcompany.com" :class="{ 'border-[#E2725B]': form.website }" />
                <svg v-if="form.website" class="absolute right-3 top-3.5 w-4 h-4 text-green-500" fill="currentColor"
                  viewBox="0 0 20 20">
                  <path fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd" />
                </svg>
              </div>
            </div>
          </div>

          <!-- Project Description -->
          <div>
            <label class="block text-gray-700 font-medium mb-2 text-sm">
              How can we help you? <span class="text-[#E2725B]">*</span>
            </label>
            <textarea v-model="form.message" name="message" required rows="3"
              class="w-full px-4 py-3 border-2 border-gray-200 rounded-lg focus:border-[#E2725B] transition-all duration-300 resize-none"
              placeholder="Tell us about your project..." :class="{ 'border-[#E2725B]': form.message }"></textarea>
          </div>

          <!-- Submit Button -->
          <div class="pt-4">
            <button type="submit" :disabled="isSubmitting || completionPercentage < 60"
              class="w-full bg-gradient-to-r from-[#E2725B] to-[#d65a42] hover:from-[#d65a42] hover:to-[#c54a32] text-white font-bold py-4 px-6 rounded-xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-lg disabled:opacity-50 disabled:cursor-not-allowed disabled:transform-none text-lg relative overflow-hidden group">
              <span v-if="!isSubmitting" class="flex items-center justify-center gap-2">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M13 10V3L4 14h7v7l9-11h-7z" />
                </svg>
                YES, I WANT TO GROW MY BUSINESS! 🚀
              </span>
              <span v-else class="flex items-center justify-center gap-2">
                <svg class="w-5 h-5 animate-spin" fill="none" viewBox="0 0 24 24">
                  <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                  <path class="opacity-75" fill="currentColor"
                    d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z">
                  </path>
                </svg>
                Sending...
              </span>
            </button>

            <p class="text-center text-xs text-gray-500 mt-3">
              🔒 Your information is secure and will never be shared
            </p>
          </div>

        </form>
      </div>

    </div>
  </div>
</template>

<script setup>
import { reactive, ref, computed } from 'vue'

const props = defineProps({
  isModalOpen: {
    type: Boolean,
    default: false
  }
})

const emit = defineEmits(['close'])

const isSubmitting = ref(false)
const showSuccess = ref(false)
const showError = ref(false)

const form = reactive({
  firstName: '',
  contactNumber: '',
  email: '',
  website: '',
  message: ''
})

const isValidEmail = computed(() => {
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
  return emailRegex.test(form.email)
})

const completionPercentage = computed(() => {
  const fields = ['firstName', 'contactNumber', 'email', 'message']
  const filledFields = fields.filter(field => form[field].trim() !== '').length
  const optionalFields = form.website ? 1 : 0
  return Math.round(((filledFields + optionalFields) / 5) * 100)
})

function closeModal() {
  emit('close')
  showSuccess.value = false
  showError.value = false
  // Reset form
  Object.keys(form).forEach(key => {
    form[key] = ''
  })
}

const submitForm = async () => {
  isSubmitting.value = true
  showSuccess.value = false
  showError.value = false

  const formData = new FormData()
  formData.append('access_key', '8bda25da-92e4-4666-bb22-51e11011ae20')
  formData.append('name', form.firstName)
  formData.append('email', form.email)
  formData.append('phone', form.contactNumber)
  formData.append('website', form.website)
  formData.append('message', form.message)
  formData.append('subject', `New Project Inquiry from ${form.firstName}`)

  try {
    const response = await fetch('https://api.web3forms.com/submit', {
      method: 'POST',
      body: formData
    })

    const data = await response.json()

    if (data.success) {
      showSuccess.value = true
      // Auto close after 3 seconds
      setTimeout(() => {
        closeModal()
      }, 3000)
    } else {
      throw new Error(data.message || 'Failed to send')
    }

  } catch (error) {
    console.error('Error:', error)
    showError.value = true
  } finally {
    isSubmitting.value = false
  }
}
</script>