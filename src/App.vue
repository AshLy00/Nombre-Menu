<script setup>
import MenuView from './views/MenuView.vue';
</script>

<template>
  <header class="center">
    <h1 class="logo">NOMBRE</h1>
    <div class="line"></div>
    <p class="text_logo">RESTAURANTE</p>
    <div class="menu_text">
      <p class="text_logo">MENÚ</p>
    </div>
  </header>
  <main>
    <MenuView />
  </main>
  <footer>
    <p class="text_footer text_footer">
      DOMICILIOS <span class="guion">-</span> 3157365656
    </p>
  </footer>
</template>

<style scoped>
.logo {
  font-size: 6rem;
  margin-bottom: 1rem;
  margin-top: 1.5rem;
}
.center {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.line {
  width: 600px;
  height: 2px;
  background-color: grey;
}
.text_logo {
  font-weight: 100;
  margin: 1rem;
  font-size: 2rem;
  letter-spacing: 20px;
}
.menu_text {
  padding: 10px;
  margin-top: 30px;
  margin-bottom: 10px;
  text-align: center;
  background-color: black;
  width: 100%;
  color: white;
}
.text_footer {
  font-weight: 100;
  font-size: 1.5rem;
  letter-spacing: 20px;
  padding: 30px;
  text-align: center;
  background-color: black;
  color: white;
  margin-top: 10px;
}

footer {
  height: 20px;
  margin-top: 10px;
  background-color: red !important;
}

@media screen and (max-width: 600px) {
  .logo {
    font-size: 3.2rem;
    margin: 1.2rem;
    margin-bottom: 0.3rem;
  }
  .text_logo {
    font-size: 1rem;
    letter-spacing: 8px;
    margin: 0.8rem;
  }
  .line {
    width: 300px;
  }
  .menu_text {
    padding: 0px;
    margin-top: 10px;
    margin-bottom: 20px;
  }
  footer {
    margin-top: 20px;
  }
  .text_footer {
    font-size: 0.9rem;
    letter-spacing: 5px;
    padding: 25px;
  }
}
</style>
