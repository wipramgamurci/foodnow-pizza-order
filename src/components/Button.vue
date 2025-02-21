<template>
  <div class="button" @click="handleClick">
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
const handleClick = () => {
  console.log("clicked");
};
</script>

<style lang="scss" scoped>
@use "./../styles/_mixins.scss";

.button {
  // display: inline-block;
  background-color: var(--primary-color);
  padding: 14px 43.5px;
  border-radius: 50px;
  cursor: pointer;
  color: var(--text-white);
  font-weight: 700;
  @include mixins.text-lg;

  &:hover {
    background-color: #c16515;
  }
}
</style>
