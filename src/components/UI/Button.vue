<template>
  <button :style="{ backgroundColor: background }" class="btn">
    <slot/>
  </button>
</template>

<script setup>
const props = defineProps({
  background: {
    type: String,
    required: false
  }
});
</script>

<style lang="scss" scoped>
.btn {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 56px;
  padding: 0 32px;
  font-size: 16px;
  color: #fff;
  background-color: rgba(249, 249, 249, 0.15);
  cursor: pointer;
  border: none;
  // width: 157px;
  // height: 56px;
  // padding-top: 16px;
  // padding-bottom: 16px;
  // font-family: inherit;
  // font-style: normal;
  // font-weight: 400;
  // font-size: 16px;
  // line-height: 1.5;
  // text-align: center;
  // text-decoration: none;
  // color: #FFFFFF;
  // background-color: rgba(249, 249, 249, 0.15);
  // box-sizing: border-box;

  &:hover {
    opacity: 0.8;
  }

}
</style>