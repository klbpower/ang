<template>
    <h2>Coche - Options API</h2>
    <p>Marca: {{brand}} </p>    
    <p>Modelo:{{model}} </p>
    <p>Power: {{power}} </p>
    <button @click="upPower(1000)">Aumentar</button>
    <button @click="downPower(100)">Disminuir</button>

   
</template>

<script>

export default{
  data(){
      return{
            brand : "Audi",
            model : "A4",
            power: 50,
      };
    },
    methods:{
        upPower( newPower ){
            console.log("Aumentando Potencia", newPower);
        },
        downPower(newPower){
            console.log("Disminuyendo potencia", newPower);
        },
    }
            
     
  
}; 
</script>

<style scoped>

</style>