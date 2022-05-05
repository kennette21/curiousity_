<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <header>
    <div class="flex justify-between pb-5 mb-10 border-b-4">
      <h1 class="font-black text-7xl">Curiousity_</h1>

      <nav class="flex gap-5">
        <RouterLink activeClass="text-purple-700" class="font-medium text-4xl hover:underline" to="/">Home</RouterLink>
        <RouterLink activeClass="text-purple-700" class="font-medium text-4xl hover:underline" to="/course">Course</RouterLink>
      </nav>
    </div>
  </header>
</template>