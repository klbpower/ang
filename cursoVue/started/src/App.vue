<template>
  <h1>Vue JS</h1>
  <Car :power="power" :upPower="upPower" />
</template>

<script>
import { ref } from "vue";
import Car from "./components/Car.vue";

export default {
  components: {
    Car,
  },
  setup() {
    let power = ref(30);

    const upPower = () => {
      power.value++;
      console.log(" Aumentar potencia");
    };

    return {
      power,
      upPower,
    };
  },
};
</script>

<style></style>
