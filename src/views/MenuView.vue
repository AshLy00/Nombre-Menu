<script setup>
import MenuCard from './../components/MenuCard.vue';
import { products } from './../database/card_database.js';
</script>

<template>
  <div class="card_container">
    <MenuCard v-for="p in products" :product="p" />
  </div>
</template>

<style scoped>
.card_container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  justify-items: center;
  row-gap: 30px;
  column-gap: 30px;
  padding: 30px;
}

@media screen and (max-width: 1650px) {
  .card_container {
    grid-template-columns: repeat(3, 1fr);
  }
}
@media screen and (max-width: 1140px) {
  .card_container {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media screen and (max-width: 600px) {
  .card_container {
    grid-template-columns: repeat(1, 1fr);
    padding: 10px;
  }
}
</style>
