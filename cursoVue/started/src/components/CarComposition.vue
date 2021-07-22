<template>
    <h2>Coche - Car Composition API</h2>
    <p>Marca: {{brand}}</p>    
    <p>Modelo: {{model}}</p>
    <p>Potencia: {{power}}</p>
    <button @click="upPower(1000)">Aumentar</button>
    <button @click="downPower(1000)">Disminuir</button>
</template>

<script>

export default{
  setup(){
      const brand = "Audi";
      const model = "A4";
      const power = 40;
          
      const upPower = () => {
          console.log("Aumentar", power);
      }
      const downPower = () => {
          console.log("Disminuir", power);
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