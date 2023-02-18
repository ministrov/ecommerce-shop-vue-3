<template>
  <div class="container">
    <Header/>
    <Hero/>
    <Advantages/>
    <Products/>
    <Ideas/>
    <Subscription/>
    <Footer/>
  </div>
</template>

<script setup>
import Header from '@/components/Layout/Header.vue'
import Footer from '@/components/Layout/Footer.vue'
import Hero from '@/components/Hero.vue'
import Advantages from '@/components/Advantages.vue'
import Products from '@/components/Products.vue'
import Ideas from '@/components/Ideas.vue'
import Subscription from '@/components/Subscription.vue'
</script>