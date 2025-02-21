<script setup lang="ts">
import Button from "./Button.vue";
</script>

<template>
  <div class="header">
    <img src="./../assets/logo.svg" alt="logo" />
    <ul class="nav-list">
      <li class="nav-item"><a href="">Home</a></li>
      <li class="nav-item nav-item--active"><a href="">Order</a></li>
      <li class="nav-item"><a href="">About</a></li>
      <li class="nav-item"><a href="">Blog</a></li>
      <li class="nav-item"><a href="">Contact us</a></li>
    </ul>
    <div class="action">
      <a href="">Login</a>
      <Button>Register</Button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "./../styles/_mixins.scss";

.header {
  width: 85vw;
  @include mixins.x-center-absolute;
  padding: 24px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;

  a {
    color: var(--text-white);
    text-decoration: none;
    @include mixins.text-lg;
    font-weight: 700;

    &:hover {
      color: var(--primary-color);
    }
  }

  .nav-list {
    display: flex;
    gap: 30px;

    .nav-item {
      list-style: none;

      &--active {
        a {
          color: var(--primary-color);
        }
      }
    }
  }

  .action {
    display: flex;
    align-items: center;
    gap: 30px;
  }
}
</style>
