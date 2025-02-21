<script setup lang="ts">
import Card from "./components/Card.vue";
import Button from "./components/Button.vue";
</script>

<template>
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
</template>

<style lang="scss" scoped>
@use "./styles/_mixins.scss";

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
</style>
