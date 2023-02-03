<script setup>
import Header from '@/components/Layout/Header.vue'
import Hero from '@/components/Hero.vue'
import Advantages from '@/components/Advantages.vue'
import Products from '@/components/Products.vue'
</script>

<template>
  <div class="container">
    <Header/>
    <Hero/>
    <Advantages/>
    <Products/>
  </div>
</template>

<style lang="scss" scoped>
.container {
  max-width: 1440px;
  margin: auto;
}
</style>
