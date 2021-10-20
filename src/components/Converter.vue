<template>
  <div>
    <h1>Conversor de Moedas</h1>

    <div class="conversor">
      <h2>{{ moedaA }} para {{ moedaB }}</h2>
      <input type="text" v-model="moedaA_value" v-on:keyup="converter" />

      <h3>{{ moedaB_value }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "conversor",
  props: ["moedaA", "moedaB"],
  data() {
    return {
      moedaA_value: "",
      moedaB_value: 0,
    };
  },

  methods: {
    converter() {
      let contação = 5.2164;

      if (this.moedaA === "USD" && this.moedaB === "BRL") contação = 5.2164;
      if (this.moedaA === "EUR" && this.moedaB === "BRL") contação = 6.397;
      if (this.moedaA === "EUR" && this.moedaB === "USD") contação = 1.2206;
      const iof_value = 0.011;
      const fx_value = 0.1;
      let valorParcial = parseFloat(this.moedaA_value) - iof_value - fx_value;
      let conversão = (valorParcial * contação).toFixed(2);
      this.moedaB_value = conversão === "NaN" ? 0 : conversão;
    },
  },
};
</script>

<style>
.conversor {
  border: 1px solid #000000;
  border-radius: 8px;
  color: #fff;
  background: #58555a;
}
</style>
