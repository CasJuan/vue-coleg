<template>
    <h2>Coche - Composition API</h2>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>

    <p> Potencias : {{ power }}</p>
    <button @click="upPower(20)">Aumentar</button>
    <button @click="downPower">Disminuir</button>

    <!-- <template  v-for="(power, index) in powers" :key="index">
        <li v-if="power < 300">Urbana: {{ power }}</li>
        <li v-else-if="power === 280">Hibrido: {{ power }}</li>
        <li v-else>Carrera: {{ power }}</li>
    </template>
 -->

</template>

<script>
import {ref} from "vue";

export default {
    setup () {
        const brand = "Audi";
        const model = "A4";
        const colors = ["Azul", "Rojo", "Morado", "Amarrillo"];
        const price = 45000;
        /* const powers = [60, 80 ,120, 16, 200, 280, 300, 390, 540, 500]; */
        let power = ref(40);

        const upPower = (newPower) => {
            console.log("Aumentar potencia...");
            power.value = power.value + newPower;
        }

        const downPower = () => {
            console.log("Bajar potencia...")
            power.value--;
        }

        return {
            brand,
            model,
            colors,
            price,
            power,
            upPower,
            downPower,
        };
    },

};
</script>

<style>

</style>