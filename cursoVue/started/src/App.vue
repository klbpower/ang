<template>
<h1>Vue JS</h1>
<CarOptions/>
<hr />
<CarComposition/>

</template>

<script>
import CarComposition from './components/CarComposition.vue';
import CarOptions from './components/CarOptions';

export default {
 components:{
   CarComposition,
   CarOptions,
 }
}
</script>

<style>

</style>
