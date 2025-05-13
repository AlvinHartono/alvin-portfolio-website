<script setup>
import Navbar from './components/MyNavbar.vue'
import HeroSection from './components/HeroSection.vue'
</script>

<template>
  <div class="bg-gray-900 text-white min-h-screen">
    <Navbar />
    <HeroSection />
    <main class="p-8">
      <section id="about" class="h-screen pt-16">
        <h2 class="text-2xl font-semibold">About Me</h2>
      </section>
      <section id="projects" class="h-screen pt-16">
        <h2 class="text-2xl font-semibold">Projects</h2>
      </section>
      <section id="education" class="h-screen pt-16">
        <h2 class="text-2xl font-semibold">Education</h2>
      </section>
      <section id="skills" class="h-screen pt-16">
        <h2 class="text-2xl font-semibold">Skills</h2>
      </section>
      <section id="contact" class="h-screen pt-16">
        <h2 class="text-2xl font-semibold">Contact</h2>
      </section>
    </main>
  </div>
</template>

<style scoped>
.min-h-screen {
  min-height: 100vh;
}
html {
  scroll-behavior: smooth;
}
</style>
