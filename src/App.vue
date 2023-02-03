<script setup>
import Header from '@/components/Layout/Header.vue'
import Hero from '@/components/Hero.vue'
</script>

<template>
  <div class="container">
    <Header/>
    <Hero/>
  </div>
</template>

<style lang="scss" scoped>
.container {
  max-width: 1440px;
  margin: auto;
}
</style>
