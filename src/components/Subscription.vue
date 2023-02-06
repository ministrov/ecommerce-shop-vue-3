<template>
  <section class="subscription">
    <div class="subscription__content">
      <h2 class="subscription__title">Join the club and get the benefits</h2>
      <p class="subscription__text">Sign up for our newsletter and receive exclusive offers on new ranges, sales, pop up stores and more</p>

      <div class="subscription__checks">
        <ul class="subscription__check-list">
          <li class="subscription__check-item">
            <img class="subscription__check-icon" src="/svg/check.svg" alt="check">
            <span class="subscription__check-name">Exclusive offers</span>
          </li>
          <li class="subscription__check-item">
            <img class="subscription__check-icon" src="/svg/check.svg" alt="check">
            <span class="subscription__check-name">Free events</span>
          </li>
          <li class="subscription__check-item">
            <img class="subscription__check-icon" src="/svg/check.svg" alt="check">
            <span class="subscription__check-name">Large discounts</span>
          </li>
        </ul>
      </div>

      <form class="subscription__subscribe-form subscribe-form">
        <input type="text" class="subscribe-form__input input-text" placeholder="your@email.com">
        <Button>
          Sign up
        </Button>
      </form>
    </div>
  </section>
</template>

<script setup>
import Button from '@/components/UI/Button.vue';
</script>

<style lang="scss" scoped>
.subscription {
  padding-top: 97px;
  padding-bottom: 86px;
  height: 444px;
  background-color: teal;
  background-image: url('/img/subscription-bg.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;

  &__content {
    max-width: 494px;
    margin: 0 auto;
  }

  &__title {
    margin: 0;
    margin-bottom: 12px;
    font-family: var(--clash);
    font-style: normal;
    font-weight: 400;
    font-size: 32px;
    line-height: 1.4;
    color: #FFFFFF;
  }

  &__text {
    max-width: 451px;
    margin: 0;
    margin-bottom: 30px;
    font-family: var(--satoshi);
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    text-align: center;
    line-height: 1.5;
    color: #FFFFFF;
  }

  &__checks {
    display: flex;
    justify-content: center;
    margin-bottom: 40px;
  }

  &__check-list {
    display: flex;
    flex-wrap: wrap;
    gap: 36px;
    margin: 0;
    padding: 0;
    list-style: none;
  }

  &__check-item {
    display: flex;
    gap: 8px;
  }

  &__check-name {
    font-family: var(--satoshi);
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 1.5;
    color: #FFFFFF;
  }

  &__subscribe-form {
    display: flex;
  }
}

.subscribe-form__input {
  flex-grow: 1;
}
</style>