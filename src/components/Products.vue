<template>
  <section class="products">
    <div class="products__elements">
      <Product
        v-for="product in products"
        :key="product.id"
        :img="product.img"
        :title="product.title"
        :price="product.price"
      />
    </div>
    <a class="products__btn">View collection</a>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import Product from '@/components/Product.vue';

const products = ref([
  {
    id: 1,
    img: '/img/product-1.jpg',
    title: 'The Dandy chair',
    price: 250
  },
  {
    id: 2,
    img: '/img/product-2.jpg',
    title: 'Rustic Vase Set',
    price: 155
  },
  {
    id: 3,
    img: '/img/product-3.jpg',
    title: 'The Silky Vase',
    price: 125
  },
  {
    id: 4,
    img: '/img/product-4.jpg',
    title: 'The Lucy Lamp',
    price: 399
  }
]);
</script>

<style lang="scss" scoped>
.products {
  &__elements {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    column-gap: 20px;
    margin-bottom: 48px;
  }

  &__btn {
    display: block;
    width: 157px;
    height: 56px;
    margin: 0 auto;
    padding-top: 16px;
    padding-bottom: 16px;
    font-family: inherit;
    text-align: center;
    line-height: 1.5;
    color: #2A254B;
    background-color: #F9F9F9;
    box-sizing: border-box;
  }
}
</style>