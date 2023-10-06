<script setup>
const props = defineProps({
  product: {
    type: Object,
  },
});
</script>

<template>
  <div class="card" :class="`${product.available ? '' : 'agotado'}`">
    <div class="card_text">
      <p class="bold">{{ product.product }}</p>
      <p class="light">
        {{ product.description }}
      </p>
      <p class="bold card_text_price">{{ product.price }}</p>
    </div>
    <div class="card_img_container">
      <div class="disponible">NO DISPONIBLE</div>
      <img :src="product.image_url" alt="product image" />
    </div>
  </div>
</template>

<style scoped>
.agotado .disponible {
  z-index: 8;
  position: absolute;
  top: 43%;
  left: 19%;
  color: white;
  display: initial;
}
.disponible {
  display: none;
}
.card {
  border: solid 1px lightgrey;
  border-radius: 20px;
  width: 350px;
  height: 190px;
  display: flex;
  align-items: center;
  transition-property: width;
  transition-duration: 0.7s;
}
.card_img_container {
  width: 260px;
  height: 190px;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
  overflow: hidden;
  display: flex;
  transition-property: width;
  transition-property: height;
  transition-duration: 0.2s;
}

img {
  object-fit: cover;
  width: 100%;
  height: 100%;
}

.agotado .card_img_container {
  filter: grayscale(100%);
}

.card_text {
  margin: 15px;
  margin-right: 10px;
  width: 190px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: start;
  transition-property: font-size;
  transition-duration: 0.7s;
}

.agotado .card_text_price {
  color: grey;
  text-decoration: line-through;
}
.agotado .card_text {
  color: grey;
}

.card_text p {
  margin: 5px;
  padding-right: 10px;
  padding-left: 15px;
}
.light {
  font-weight: 100;
  font-size: 0.7rem;
  transition-property: font-size;
  transition-duration: 0.7s;
}

.bold {
  font-size: 1.1rem;
  transition-property: font-size;
  transition-duration: 0.7s;
}

@media screen and (max-width: 360px) {
  .card {
    width: 300px;
    height: 150px;
  }
  .card_img_container {
    width: 450px;
    height: 150px;
  }
  .light {
    font-weight: 100;
    font-size: 0.5rem;
  }
  .bold {
    font-size: 0.8rem;
  }
}

@media screen and (max-width: 600px) {
  .card {
    width: 310px;
    height: 160px;
  }
  .card_img_container {
    width: 220px;
    height: 160px;
  }
  .light {
    font-weight: 100;
    font-size: 0.7rem;
  }
  .bold {
    font-size: 0.9rem;
  }
  .agotado .disponible {
    top: 43%;
    left: 15%;
    font-size: 0.9rem;
  }
}
</style>
