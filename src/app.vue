<script setup>
import NavBar from '@/components/nav/NavBar.vue';
</script>

<template>
  <header class="fixed top-0 z-10 w-full">
    <div class="container mx-auto flex justify-end">
      <NavBar />
    </div>
  </header>
  <router-view />
</template>
