<template>
  <main
    class="container mx-auto mt-[12rem] px-4 py-16 xl:mt-16">
    <Tasks />
  </main>
</template>

<style>
body {
  @apply dark:bg-gray-900 dark:text-gray-50;
}
</style>
<script setup>
import Tasks from '@/components/tasks/Tasks.vue';
</script>
