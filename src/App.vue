<script>
import Calculadora from "./components/Calculadora.vue";

export default {
  name: "App",
  components: {
    Calculadora,
  },
};
</script>

<template>
  <div id="app">
  <div class="box">
    <p>CALCULADORA</p>
    <Calculadora />
  </div>
</div>
</template>

<style>
body {
  background-color: #005791;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20vh;
}

.box {
  background-color: #5892b9;
  padding: 40px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  width: 300px;
  margin: 0 auto;
  text-align: center; /* Centraliza o conteúdo na caixa */
}

input {
  margin: 5px; /* Espaçamento entre os inputs */
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  width: 100px;
}

.box p {
  font-size: 18px;
  font-weight: bold;
  color: #fff;
}

.box a {
  text-decoration: none;
  background-color: #e74c3c;
  color: #fff;
  padding: 5px 10px;
  border-radius: 5px;
}

.box a:hover {
  background-color: #c0392b;
}
</style>
