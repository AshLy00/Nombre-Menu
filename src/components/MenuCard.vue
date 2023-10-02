<script setup></script>

<template>
  <div class="card" :class="`${false ? '' : 'agotado'}`">
    <div class="card_text">
      <p class="bold">Pasta Boloñesa</p>
      <p class="light">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, lorem ipsum
        dolor sit amet, consectetur adipiscing elit.
      </p>
      <p class="bold card_text_price">$23.000</p>
    </div>
    <div class="card_img_container">
      <img
        src="https://www.thewholesomedish.com/wp-content/uploads/2018/07/Best-Lasagna-550-500x375.jpg"
        alt="product image"
      />
    </div>
  </div>
</template>

<style scoped>
.card {
  border: solid 1px lightgrey;
  border-radius: 20px;
  width: 500px;
  height: 250px;
  display: flex;
  align-items: center;
}
.card_img_container {
  width: 738px;
  height: 250px;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
  overflow: hidden;
  display: flex;
}

.agotado .card_img_container {
  filter: grayscale(100%);
}

.card_text {
  margin: 25px;
  margin-right: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: justify;
}

.agotado .card_text_price {
  color: grey;
  text-decoration: line-through;
}
.agotado .card_text {
  color: grey;
}

.card_text p {
  margin: 10px;
}
.light {
  font-weight: 100;
  font-size: 1rem;
}

.bold {
  font-size: 1.2rem;
}
</style>
