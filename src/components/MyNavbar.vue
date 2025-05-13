<script setup>
// No specific script needed for this basic navbar yet
// You might add props or methods here later if needed
const yourName = 'Alvin Hartono' // Replace with your actual name
</script>

<template>
  <nav class="bg-gray-800 text-white p-4 shadow-md fixed w-full top-0 left-0 z-50">
    <div class="container mx-auto flex justify-between items-center">
      <a href="#app" class="text-xl font-bold hover:text-blue-400 transition-colors">{{
        yourName
      }}</a>

      <ul class="flex space-x-6">
        <li><a href="#about" class="hover:text-blue-400 transition-colors">About</a></li>
        <li><a href="#projects" class="hover:text-blue-400 transition-colors">Projects</a></li>
        <li><a href="#education" class="hover:text-blue-400 transition-colors">Education</a></li>
        <li><a href="#skills" class="hover:text-blue-400 transition-colors">Skills</a></li>
        <li><a href="#contact" class="hover:text-blue-400 transition-colors">Contact</a></li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
/* Scoped styles specific to Navbar.vue */
/* For example, if you need custom styles not easily achievable with Tailwind */
/* The 'fixed', 'w-full', 'top-0', 'left-0', 'z-50' classes make the navbar stick to the top */
</style>
