<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <Converter moeda-a="USD" moeda-b="BRL" />
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
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
