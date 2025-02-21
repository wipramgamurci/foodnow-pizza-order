<script setup lang="ts">
import Header from "./components/Header.vue";
import PizzaCard from "./components/PizzaCard.vue";

import PizzaList from "./data/pizza-list.json";

const pizzaList = PizzaList.data;
</script>

<template>
  <Header />
  <div class="hero">
    <p>Pizza order</p>
  </div>
  <div class="container">
    <div class="left">
      <h1>Chose your pizza</h1>
      <div class="pl">
        <PizzaCard v-for="pizza in pizzaList" :key="pizza.id" :pizza="pizza" />
      </div>
      <h1>Custom pizza</h1>
    </div>
    <div class="right">right</div>
  </div>
  <div class="filler"></div>
</template>

<style lang="scss" scoped>
@use "./styles/_mixins.scss";

.pl {
  display: flex;
  gap: 30px;
}

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

.container {
  width: 85vw;
  margin: 160px auto;
  // @include mixins.x-center-absolute;

  display: flex;
  gap: 100px;

  h1 {
    @include mixins.text-5xl;
    font-weight: 700;
    color: var(--primary-color);
  }
}
</style>
