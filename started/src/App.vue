<template>
  <h1>Vue JS</h1>
  <CarComposition />
  <hr/>
  <CarOptions/>
  <hr/>
  <Car :power="power" :upPower="upPower"/>
</template>

<script>
import {ref} from 'vue';

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
    let power = ref(36);

    const upPower = () => {
      console.log("Aumentar power");
      power.value++
    }

    return{
      power,
      upPower,
    }
  }
};
</script>

<style></style>
