<script setu></script>

<template>
  <div class="card" :class="`${true ? '' : 'agotado'}`">
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
        src="https://assets.delirec.com/images%2Fr2UlVN42QjXxE3RvkOpqTYn0Sis2%2Frecipe%2F92c7366a-3743-4e03-b6e5-1d7d1a0dc45f-Lasanha-de-Carne-mo%C3%ADda%F0%9F%8D%9D-gallery-0"
        alt="product image"
      />
    </div>
  </div>
</template>

<style scoped>
.card {
  border: solid 1px lightgrey;
  border-radius: 20px;
  width: 350px;
  height: 190px;
  display: flex;
  align-items: center;
}
.card_img_container {
  width: 520px;
  height: 190px;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
  overflow: hidden;
  display: flex;
}

.agotado .card_img_container {
  filter: grayscale(100%);
}

.card_text {
  margin: 15px;
  margin-right: 5px;
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
  margin: 7px;
  padding-right: 15px;
  padding-left: 5px;
}
.light {
  font-weight: 100;
  font-size: 0.7rem;
}

.bold {
  font-size: 1.1rem;
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
</style>
