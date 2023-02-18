<template>
  <section class="products">
    <h2 class="visually-hidden">Cards of the product</h2>
    <div class="products__elements">
      <Product
        v-for="product in products"
        :key="product.id"
        :img="product.img"
        :title="product.title"
        :price="product.price"
      />
    </div>
    <Button
      color="lightgray"
      type="Link"
      to="to"
    >
      View collection
    </Button>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import Product from '@/components/Product.vue';
import Button from '@/components/UI/Button.vue';

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

    @media screen and (max-width: 1024px) {
      grid-template-columns: repeat(2, 1fr);
      row-gap: 20px;
    }
  }

  & > a {
    max-width: 182px;
    margin: 0 auto;
  }
}
</style>