<template>
  <section class="hero">
    <h2 class="visually-hidden">Hero section</h2>
    <img class="hero-img" src="/img/hero-bg.jpg" width="1440" height="704" alt="hero-bg">
    <div class="hero-info">
      <h3>Luxury homeware for people who love timeless design quality</h3>
      <p>Shop the new Spring 2022 collection today</p>

      <Button
        color="lightgray"
        type="Link"
        to="/"
        class="hero__btn"
      >
        View collection
      </Button>
    </div>
  </section>
</template>

<script setup>
import Button from '@/components/UI/Button.vue'
</script>

<style lang="scss" scoped>
.hero {
  position: relative;
  max-height: 704px;

  &-info {
    position: absolute;
    display: flex;
    flex-direction: column;
    bottom: 134px;
    right: 73px;
    width: 630px;
    height: 444px;
    padding-top: 48px;
    padding-bottom: 46px;
    padding-left: 56px;
    padding-right: 61px;
    background-color: #fff;

    h3 {
      max-width: 513px;
      margin: 0;
      margin-bottom: 20px;
      font-family: var(--clash);
      font-size: 32px;
      font-weight: 400;
      line-height: 1.4;
      color: #22202E;
    }

    p {
      margin: 0;
      margin-bottom: 157px;
      font-family: inherit;
      font-size: 18px;
      line-height: 1.5;
      color: #5B5676;
    }
  }

  &-img {
    max-width: 100%;
  }
}
</style>