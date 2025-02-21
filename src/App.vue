<script setup lang="ts">
import Card from "./components/Card.vue";
import Button from "./components/Button.vue";
import Header from "./components/Header.vue";
</script>

<template>
  <Header />
  <div class="hero">
    <p>Pizza order</p>
  </div>
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
