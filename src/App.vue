<template>
  <div class="min-h-screen flex flex-col">
    <Header />
    <main class="flex-1 container mx-auto p-5">
      <RouterView />
    </main>
    <Footer />
  </div>
</template>

<script setup lang="ts">
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
</script>