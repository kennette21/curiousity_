<script setup>
import { RouterView } from 'vue-router'
import Header from './components/Header.vue';
</script>

<template>
  <div class="m-12">
    <Header />

    <RouterView />
  </div>
</template>
