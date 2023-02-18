<template>
  <section class="advantages">
    <h2 class="advantages__title">Whate makes our brand different</h2>

    <div class="advantages__elements">
      <div
        v-for="(element, i) in advantages"
        :key="i"
        class="advantages__element advantages__element--delivery"
      >
        <img :src="element.img" :alt="element.title">
        <h3>{{ element.title }}</h3>
        <p>{{ element.description }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import {ref} from 'vue';

const advantages = [
  {
    img: '/svg/advantages-1.svg',
    title: 'Next day as standard',
    description: 'Order before 3pm and get your order the next day as standard'
  },
  {
    img: '../../public/svg/advantages-2.svg',
    title: 'Made by true artisans',
    description: 'Handmade crafted goods made with real passion and craftmanship'
  },
  {
    img: '../../public/svg/advantages-3.svg',
    title: 'Unbeatable prices',
    description: 'For our materials and quality you won’t find better prices anywhere'
  },
  {
    img: '../../public/svg/advantages-4.svg',
    title: 'Recycled packaging',
    description: 'We use 100% recycled to ensure our footprint is more manageable'
  }
];
</script>

<style lang="scss" scoped>
.advantages {
  padding-top: 80px;
  padding-bottom: 82px;

  &__title {
    margin: 0;
    margin-bottom: 36px;
    font-family: var(--clash);
    font-weight: 400;
    font-size: 24px;
    line-height: 1.5;
    text-align: center;
    color: #2A254B;
  }

  &__elements {
    display: flex;
    gap: 22px;
  }

  &__element {
    padding: 48px;
    background-color: #F9F9F9;

    img {
      display: block;
      margin-bottom: 12px;
    }

    h3 {
      margin: 0;
      margin-bottom: 12px;
      font-family: 'Clash Display', sans-serif;
      font-weight: 400;
      font-size: 20px;
      line-height: 1.4;
      color: #2A254B;
    }

    p {
      margin: 0;
      padding-right: 22px;
      font-family: inherit;
      font-size: inherit;
      color: #2A254B;
    }
  }
}
</style>