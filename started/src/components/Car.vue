<template>
    <h2>Coche</h2>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Color: 
        <!-- <span v-for="(color, index) in colors" :key="index" >
            {{index}}: {{ color }} -
        </span> -->

        <ul>
            <li span v-for="(color, index) in colors" :key="index">
                {{index}}: {{ color }}
            </li>
        </ul>

    </p>
    <p>Precio: {{ price }}</p>
    <p>Potencia: {{ power }}</p>
    <p>Mensaje: {{ mensaje.title }}</p>
</template>

<script>
export default {
    setup () {
        const brand = "Audi";
        const model = "A4";
        const colors = ["Azul", "Rojo", "Morado", "Amarrillo"];
        const price = 45000;
        const powr = 240;
        const mensaje = {
            title: "Estoy bien",
            text: "Welcome",
        }

        return {
            brand,
            model,
            colors,
            price,
            powr,
            mensaje,
        };
    },

};
</script>

<style>

</style>