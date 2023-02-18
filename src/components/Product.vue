<template>
  <router-link to="/" class="product">
    <article class="product__elem">
      <img class="product__img" :src="img" :alt="title">
      <router-link to="/" class="product__title">{{ title }}</router-link>
      <span class="product__span">£{{ price }}</span>
    </article>
  </router-link>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  img: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  price: {
    type: Number,
    required: true
  }
});
</script>

<style lang="scss" scoped>
.product {
  text-decoration: none;
  color: transparent;

  &__elem {
    display: flex;
    flex-direction: column;
  }

  img {
    display: block;
    margin-bottom: 24px;
  }

  &__title {
    margin: 0;
    margin-bottom: 8px;
    font-family: var(--clash);
    font-style: normal;
    font-weight: 400;
    font-size: 20px;
    line-height: 1.4;
    text-decoration: none;
    color: #2A254B;

    &:hover {
      text-decoration: underline;
    }
  }

  &__span {
    font-family: var(--satoshi);
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 1.5;
    color: #2A254B;
  }
}
</style>