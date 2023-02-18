<template>
  <button
    v-if="type === 'button'"
    :class="[
      'btn',
      {
        'btn--primary': color === 'primary',
        'btn--secondary': color === 'secondary',
        'btn--lightgray': color === 'lightgray',
        'btn--white': color === 'white',
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
    color: var(--white-main);
    background-color: var(--dark-primary);
  }

  &--secondary {
    color: var(--white-main);
    background: rgba(249, 249, 249, 0.15);
  }

  &--lightgray {
    color: var(--dark-primary);
    background-color: var(--lightgray);
  }

  &--white {
    color: var(--dark-primary);
    background-color: var(--white-main);
  }

  &:hover {
    opacity: 0.8;
  }
}
</style>
