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
  margin: 3rem;
  margin-bottom: 1rem;
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
}
.text_footer {
  padding: 30px;
  text-align: center;
  background-color: black;
  color: white;
  margin-top: 10px;
}

footer {
  height: 20px;
  background-color: red !important;
}

@media screen and (max-width: 800px) {
  .guion {
    display: none;
  }
}

@media screen and (max-width: 600px) {
  .logo {
    font-size: 4rem;
  }
  .text_logo {
    font-size: 1.5rem;
    letter-spacing: 10px;
  }

  .line {
    width: 350px;
  }
  .menu_text {
    padding: 10px;
    margin-top: 30px;
    margin-bottom: 30px;
    text-align: center;
    background-color: black;
    width: 100%;
    color: white;
  }
}
</style>
