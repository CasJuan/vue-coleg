<template>
    <h2>Coche</h2>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>

    <p> Potencias </p>

    <template  v-for="(power, index) in powers" :key="index">
        <li v-if="power < 300">Urbana: {{ power }}</li>
        <li v-else-if="power === 280">Hibrido: {{ power }}</li>
        <li v-else>Carrera: {{ power }}</li>
    </template>


</template>

<script>
export default {
    setup () {
        const brand = "Audi";
        const model = "A4";
        const colors = ["Azul", "Rojo", "Morado", "Amarrillo"];
        const price = 45000;
        const powers = [60, 80 ,120, 16, 200, 280, 300, 390, 540, 500];

        return {
            brand,
            model,
            colors,
            price,
            powers,
        };
    },

};
</script>

<style>

</style>