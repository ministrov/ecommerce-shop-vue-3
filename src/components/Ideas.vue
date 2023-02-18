<template>
  <section class="ideas">
    <h2 class="visually-hidden">Small Ideas</h2>
    <div class="ideas__text">
      <p class="ideas__text-slogan">It started with a small idea</p>
      <p class="ideas__text-descr">A global brand with local beginnings, our story begain in a small studio in South London in early 2014
      </p>

      <Button
        color="secondary"
        type="Link"
        to="/"
      >
        View collection
      </Button>
      <!-- <a class="ideas__link" href="#">View collection</a> -->
    </div>
    <div class="ideas__img">
      <img src="/img/small-room.jpg" width="630" height="478" alt="A view of the small room">
    </div>
  </section>
</template>

<script setup>
import Button from '@/components/UI/Button.vue'

</script>

<style lang="scss" scoped>
.ideas {
  display: flex;
  gap: 16px;
  padding-top: 60px;
  padding-bottom: 60px;

  &__text {
    width: 50%;
    padding-top: 64px;
    padding-bottom: 60px;
    padding-left: 64px;
    padding-right: 75px;
    background-color: #2A254B;
    box-sizing: border-box;

    &-slogan {
      max-width: 495px;
      margin: 0;
      margin-bottom: 12px;
      font-family: 'Clash Display';
      font-style: normal;
      font-weight: 400;
      font-size: 32px;
      line-height: 39px;
      color: #FFFFFF;
    }

    &-descr {
      max-width: 495px;
      margin: 0;
      margin-bottom: 205px;
      font-family: var(--satoshi);
      font-style: normal;
      font-weight: 400;
      font-size: 18px;
      line-height: 24px;
      color: #FFFFFF;
    }
  }

  &__img {
    width: 50%;

    img {
      display: flex;
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
}
</style>