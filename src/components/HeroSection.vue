<script setup>
import { onMounted, ref } from 'vue'

const name = 'Alvin Hartono'
const profession = 'Final Year University Student'
const tagline = "A short and catchy tagline about what you do or what you're passionate about."
const avatarSrc = '/img/avatar-placeholder.png'
const projectsLink = '#projects'
const resumeLink = '/resume.pdf'

// Animation state
const isContentVisible = ref(false)
const isImageVisible = ref(false)

onMounted(() => {
  // Small delay for initial page load
  setTimeout(() => {
    isContentVisible.value = true

    // Delay the image animation slightly
    setTimeout(() => {
      isImageVisible.value = true
    }, 400)
  }, 200)
})
</script>

<template>
  <section class="container mx-auto py-16 md:py-24 px-6 md:px-8">
    <div class="flex flex-col md:flex-row items-center justify-center max-w-6xl mx-auto">
      <div
        class="md:w-1/2 text-center md:text-left mb-12 md:mb-0 md:pr-8 lg:pr-12 content-container"
        :class="{ 'content-visible': isContentVisible }"
      >
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold mb-4 leading-tight">
          Hi, I'm <span class="text-blue-400">{{ name }}</span>
        </h1>
        <p class="text-xl sm:text-2xl text-gray-300 mb-6">
          {{ profession }}
        </p>
        <p class="text-lg text-gray-400 mb-8">
          {{ tagline }}
        </p>
        <div
          class="flex flex-col sm:flex-row justify-center md:justify-start space-y-4 sm:space-y-0 sm:space-x-4"
        >
          <a
            :href="projectsLink"
            class="bg-blue-500 hover:bg-blue-600 text-white font-semibold py-3 px-8 rounded-lg text-lg transition-colors duration-300 ease-in-out shadow-md hover:shadow-lg transform hover:-translate-y-0.5"
          >
            View Projects
          </a>
          <a
            :href="resumeLink"
            target="_blank"
            rel="noopener noreferrer"
            class="bg-gray-700 hover:bg-gray-600 text-white font-semibold py-3 px-8 rounded-lg text-lg transition-colors duration-300 ease-in-out shadow-md hover:shadow-lg transform hover:-translate-y-0.5"
          >
            Download Resume
          </a>
        </div>
      </div>

      <div class="md:w-1/2 flex justify-center md:justify-end">
        <div
          class="flex items-center justify-center image-container"
          :class="{ 'image-visible': isImageVisible }"
        >
          <img
            :src="avatarSrc"
            alt="Professional Avatar"
            class="rounded-full w-64 h-64 sm:w-72 sm:h-72 md:w-80 md:h-80 lg:w-96 lg:h-96 object-cover shadow-xl border-4 border-gray-700"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Animation styles */
.content-container {
  opacity: 0;
  transform: translateX(-50px);
  transition: all 0.8s ease-out;
}

.content-visible {
  opacity: 1;
  transform: translateX(0);
}

.image-container {
  opacity: 0;
  transform: translateX(50px);
  transition: all 0.8s ease-out;
}

.image-visible {
  opacity: 1;
  transform: translateX(0);
}
</style>
