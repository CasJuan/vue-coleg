<template>
    <h2>Coche</h2>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Color: {{ color[1] }}</p>
    <p>Precio: {{ price }}</p>
    <p>Potencia: {{ power }}</p>
    <p>Mensaje: {{ mensaje.title }}</p>
</template>

<script>
export default {
    /* data (){
        return{
            brand:"Audi",
            model: "A4",
            color: ["Azul", "Rojo", "Verde"],
            price: 38000,
            power: 180,
            mensaje:{
                title: "Hola mundo",
                text: "Adios",
            }
        };
    }, */
    setup () {
        const brand = "Audi";
        const model = "A4";
        const color = ["Azul", "Rojo", "Morado"];
        const price = 45000;
        const powr = 240;
        const mensaje = {
            title: "Estoy bien",
            text: "Welcome",
        }

        return {
            brand,
            model,
            color,
            price,
            powr,
            mensaje,
        };
    },

};
</script>

<style>

</style>