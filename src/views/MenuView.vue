<script>
import MenuCard from './../components/MenuCard.vue';
</script>

<template>
  <div class="card_container">
    <MenuCard />
    <MenuCard />
    <MenuCard />
  </div>
</template>

<style scoped>
.card_container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  margin-top: 80px;
  margin-bottom: 80px;
  margin-right: 300px;
  margin-left: 300px;
  justify-items: center;
  row-gap: 30px;
  column-gap: 30px;
}
</style>
