<template>
    <h2>Coche - Car Composition API</h2>
    <p>Marca: {{brand}}</p>    
    <p>Modelo: {{model}}</p>
    <p>Potencia: {{power}}</p>
    <button @click="upPower(1000)">Aumentar</button>
    <button @click="downPower(1000)">Disminuir</button>
</template>

<script>
import { ref } from "vue";
export default{
  setup(){
      const brand = "Audi";
      const model = "A4";
      let   power = ref(40);
          
      const upPower = (newPower) => {
          power.value=power.value+newPower;
          console.log("Aumentar", power.value);
      }
      const downPower = (newPower)=> {
          power.value-=newPower;
          console.log("Disminuir", power.value);
      }    
      return {
          brand,
          model,
          power,
          upPower,
          downPower,
    
      };
  },
}; 
</script>

<style scoped>

</style>