<template>
  <header class="bg-white p-4 flex items-center justify-between shadow-md">
    <!-- Logo Section -->
    <img src="/logo.png" alt="Bit of Everything Logo" class="logo w-32 h-auto" />
    
    <!-- Website Title and Phone Number Section -->
    <div class="flex flex-col items-center">
      <h1 class="text-2xl font-semibold">Bit of Everything</h1>
      <p class="text-sm text-gray-600">+92 3377022338</p>
    </div>

    <!-- Button Link -->
    <a
      href="https://boe.com.pk"
      target="_blank"
      class="bg-blue-500 text-white px-4 py-2 rounded-md hover:bg-blue-600 transition duration-300"
    >
      Visit BOE.com.pk
    </a>
  </header>
  
  <!-- Main Content -->
  <main class="min-h-screen flex flex-col items-center justify-center">
    <div class="text-center">
      <h2 class="text-3xl font-bold text-gray-800">Welcome to Bit of Everything</h2>
      <p class="text-lg text-gray-500">Your one-stop shop for everything you need!</p>
    </div>
  </main>
  
  <!-- Footer -->
  <footer class="bg-gray-800 text-white py-4 text-center">
    <p>&copy; 2025 Bit of Everything. All rights reserved.</p>
  </footer>
</template>

<script setup>
// You can add any additional logic or scripts here if needed
</script>

<style scoped>
/* Logo styling */
.logo {
  width: 120px; /* Adjust the width of the logo */
  height: auto;
}

/* Additional Styling for Main and Footer */
footer {
  font-size: 0.875rem; /* Smaller text for footer */
}

main {
  padding: 20px;
}
</style>
