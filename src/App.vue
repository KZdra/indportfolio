<script setup>
</script>

<template>
   <div>
    <nav class="bg-gray-800 py-4">
      <div class="container mx-auto flex justify-between items-center px-4">
        <!-- Logo -->
        <a href="#" class="text-white text-lg font-bold"><img src="/logo.png" alt="" width="50px"></a>
        <!-- Menu -->
        <div class="hidden md:flex space-x-4">
          <a href="#" class="text-gray-300 hover:text-white">Home</a>
          <a href="#skills" class="text-gray-300 hover:text-white">Skills</a>
          <a href="#project" class="text-gray-300 hover:text-white">Project</a>
        </div>
        <!-- Tombol "Contact Me" -->
        <button class="hidden md:block bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded">
          Contact Me
        </button>
        <!-- Tombol untuk menu responsif -->
        <div class="md:hidden">
          <button @click="toggleMobileMenu" class="text-white focus:outline-none">
            <svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
          </button>
        </div>
      </div>
      <!-- Menu responsif -->
      <div v-if="mobileMenuOpen" class="md:hidden bg-gray-800">
        <a href="#" class="block py-2 px-4 text-gray-300 hover:text-white">Home</a>
        <a href="#skills" class="block py-2 px-4 text-gray-300 hover:text-white">Skills</a>
        <a href="#project" class="block py-2 px-4 text-gray-300 hover:text-white">Project</a>
        <br>
        <button class="block w-full bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded">
          Contact Me!
        </button>
      </div>
    </nav>
  </div>
</template>


<script>export default {
  data() {
    return {
      mobileMenuOpen: false
    };
  },
  methods: {
    toggleMobileMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen;
    }
  }
};</script>