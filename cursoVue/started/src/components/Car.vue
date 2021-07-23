<template>
  <h2>Coche - Car Composition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Power: {{ power }}</p>
  <button @click="upPower">Aumentar</button>
</template>

<script>
export default {
  props: {
    power: {
      type: Number,
      default: 60,
    },
    upPower: Function,
  },

  setup(props) {
    const brand = "Audi";
    const model = "A4";

    console.log(props);

    const testPower = () => {
      props.upPower();
    };

    return {
      brand,
      model,
      testPower,
    };
  },
};
</script>

<style scoped></style>
