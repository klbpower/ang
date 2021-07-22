<template>
    <h2>Coche </h2>
    <p>Marca: {{brand}}</p>
    <p>
        Color
        <ul>
            <li v-for="(color,index) in colors" :key="index"> 
            {{index}}: {{color}}
            </li>
        </ul>
        </p>
    <p>Precio: {{price}}</p>
    <p>Potencia: {{power}}</p>
    {{message.title}} - {{message.text}}
</template>

<script>

export default{
  setup(){
      const brand = "Audi";
      const model = "A4";
      const colors = ["Blue", "Yellow", "Green", "Brown", "Black", "White", "Red", "Pink"];
      const price = 45000;
      const power = 240;
      const message = {
          title: "I am fine",
          text: "Welcome",
      };
      return {
          brand,
          model,
          colors,
          price,
          power,
          message,
      };
  },
}; 
</script>

<style scoped>

</style>