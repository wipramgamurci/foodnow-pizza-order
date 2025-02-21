<script setup lang="ts">
defineProps(["pizza"]);
</script>

<template>
  <div class="pizza-card">
    <img src="./../assets/Cheese Pizza.png" alt="" />
    <div>
      <p class="title">{{ pizza.name }}</p>
      <div class="price">
        <p v-if="pizza.discount.is_active">${{ pizza.discount.final_price }}</p>
        <p :class="{ strike: pizza.discount.is_active }">${{ pizza.price }}</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "./../styles/_mixins.scss";

.pizza-card {
  padding: 32px;
  border-radius: 8px;
  background-color: var(--text-white);
  border: 1px solid #3333331a;
  display: flex;
  gap: 32px;
  align-items: center;
  transition: background-color 0.5s ease;

  img {
    transition: transform 0.5s ease;
  }

  &:hover {
    background-color: #e77e234d;

    img {
      transform: rotate(20deg);
    }
  }

  .price {
    display: flex;
    gap: 8px;
  }

  p {
    @include mixins.text-xl;

    &.title {
      font-weight: 700;
    }

    &.strike {
      text-decoration: line-through;
      color: rgb(149, 149, 148);
    }
  }
}
</style>
