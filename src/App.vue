<template>
  <img alt="Vue logo" src="./assets/conversor.png" />
  <div class="container">
    <Converter moeda-a="USD" moeda-b="BRL" />
    <Converter moeda-a="EUR" moeda-b="BRL" />
    <Converter moeda-a="EUR" moeda-b="USD" />
  </div>
</template>

<script>
import Converter from "./components/Converter.vue";

export default {
  name: "App",
  components: {
    Converter,
  },
};
</script>

<style>
#app {
  justify-content: space-around;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#app img {
  width: 400px;
}

.container {
  display: flex;
  justify-content: space-around;
}
</style>
