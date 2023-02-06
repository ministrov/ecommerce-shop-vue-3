<template>
  <button
    v-if="type === 'button'"
    :class="[
      'btn',
      {
        'btn--primary': color === 'primary',
        'btn--secondary': color === 'secondary',
        'btn--lightgray': color === 'lightgray',
      },
    ]"
    class="btn"
  >
    <slot />
  </button>

  <router-link
    v-else
    :class="[
      'btn',
      {
        'btn--primary': color === 'primary',
        'btn--secondary': color === 'secondary',
        'btn--lightgray': color === 'lightgray',
      },
    ]"
    :to="to"
  >
    <slot />
  </router-link>
</template>

<script setup>
const props = defineProps({
  background: {
    type: String,
    required: false,
  },
  type: {
    type: String,
    default: "button",
  },
  to: {
    type: String,
    required: false,
  },
  color: {
    type: String,
    default: "primary",
  },
});
</script>

<style lang="scss" scoped>
.btn {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  max-width: 170px;
  height: 56px;
  padding-left: 32px;
  padding-right: 32px;
  font-size: 16px;
  text-decoration: none;
  cursor: pointer;
  border: none;


  &--primary {
    color: #FFFFFF;
    background-color: #2a254b;
  }

  &--secondary {
    color: #FFFFFF;
    background: rgba(249, 249, 249, 0.15);
  }

  &--lightgray {
    color: #2a254b;
    background-color: #f9f9f9;
  }

  &:hover {
    opacity: 0.8;
  }
}
</style>
