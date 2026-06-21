<template>
  <!-- O NavBar aparece em todas as páginas -->
  <NavBar />

  <!-- Aqui é renderizada a view correspondente à rota atual -->
  <main class="container py-4">
    <RouterView />
  </main>
</template>

<script setup lang="ts">
import NavBar from './components/Navbar.vue'
</script>