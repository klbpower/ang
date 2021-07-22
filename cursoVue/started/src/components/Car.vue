<template>
    <h2>Coche </h2>
    <p>Marca: {{brand}}</p>    
    <p>Modelo: {{model}}</p>
    <p>Potencias</p>
    <ul>
        <template v-for="(power, index) in powers" :key="index">
            <li v-if="power <280"> Urbana {{power}}</li>
            <li v-else-if="power === 280"> Híbrido {{power}}</li>
            <li v-else> Carrera {{power}}</li>
        </template>
    </ul>
  
</template>

<script>

export default{
  setup(){
      const brand = "Audi";
      const model = "A4";
      const powers = [60,80,120,160,200,280,300,390,540,500];
      
      return {
          brand,
          model,
          powers,
      };
  },
}; 
</script>

<style scoped>

</style>