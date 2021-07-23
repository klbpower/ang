<template>
  <h2>Coche - Car Composition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Power: {{ power }}</p>
  <button @click="upPower">Aumentar</button>
  <button @click="downPowerFn">Disminuir</button>
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

  emits: ["downPower"],

  setup(props, context) {
    const brand = "Audi";
    const model = "A4";

    const downPowerFn = () => {
      context.emit("downPower");
    };

    return {
      brand,
      model,
      downPowerFn,
    };
  },
};
</script>

<style scoped></style>
