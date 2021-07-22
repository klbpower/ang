<template>
    <h2>Coche </h2>
<p>Marca: {{brand}}</p>
<p>Color: {{color[2]}}</p>
<p>Precio: {{price}}</p>
<p>Potencia: {{power}}</p>
{{message.title}} - {{message.text}}
</template>

<script>

export default{
   data(){
       return {
           brand: "Audi",
           model:"A4",
           color:["Blue", "Orange", "Yellow", "Red", "Pink", "Brown", "Green", "Gray", "Black", "White"],
           price:38000,
           power:180,
           message: {
               title: "Hello World",
               text: "Good Bye",
           },
       };
   },
}; 
</script>

<style scoped>

</style>