<template>
  <h1>Vue JS</h1>
  <CarComposition />
  <hr/>
  <CarOptions/>
  <hr/>
  <Car :power="power"/>
</template>

<script>
import Car from "./components/Car.vue";
import CarComposition from "./components/CarComposition.vue";
import CarOptions from "./components/CarOptions.vue";

export default {
  components: {
    CarComposition,
    CarOptions,
    Car
  },
  setup(){
    let power = 38;

    return{
      power,
    }
  }
};
</script>

<style></style>
