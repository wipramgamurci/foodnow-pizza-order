<script setup lang="ts">
import Card from "./components/Card.vue";
import Button from "./components/Button.vue";
</script>

<template>
  <div class="header">
    <img src="./assets/logo.svg" alt="logo" />
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
  <div class="hero">
    <p>Pizza order</p>
  </div>
  <!-- <h1 class="hello">Hello World!</h1>
  <div class="hero">
    <h2 class="hero-text">This is a pizza order app.</h2>
    <p class="hero-description">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quod.
    </p>
  </div> -->
  <Card />
  <Button>Click me</Button>
  <div class="filler"></div>
</template>

<style lang="scss" scoped>
@use "./styles/_mixins.scss";

.filler {
  height: 100vh;
}

.hero {
  // background-color: var(--secondary-color);
  background-image: url("./assets/hero.png");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  padding: 16dvw 0;
  display: flex;
  justify-content: center;

  p {
    @include mixins.text-8xl;
    font-weight: 700;
    color: var(--primary-color);
  }
}

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
