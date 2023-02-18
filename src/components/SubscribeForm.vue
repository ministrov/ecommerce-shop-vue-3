<template>
  <form class="subscribe-form">
    <input
      type="text"
      class="subscribe-form__input input-text"
      placeholder="your@email.com"
      :style="{ backgroundColor: bgInput, color: colorText }"
    >
    <Button
      type="button"
      :color="colorButton || 'primary'"
    >
      Sign up
    </Button>
  </form>
</template>

<script setup>
import Button from '@/components/UI/Button.vue';

const props = defineProps({
  bgInput: {
    type: String,
    required: false
  },
  colorButton: {
    type: String,
    required: false
  },
  colorText: {
    type: String,
    required: false
  }
});
</script>

<style lang="scss" scoped>
.subscribe-form {
  display: flex;

  &__input {
    flex-grow: 1;
  }
}
</style>