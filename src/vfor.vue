


<script setup>
    const arrayFrutas = [
        {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
        },
        {
            name: "Pera",
            price: "$2.00",
            description: "Una pera",
        },
        {
            name: "Naranja",
            price: "$3.00",
            description: "Una naranja",
        },
    ];

    const objetoFruta = {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
        }

</script> 

<template>

<ul>
    <li v-for="fruta in arrayFrutas" :key="fruta.name"> {{ fruta }}</li>
</ul>

<ul>
    <li v-for="(value, propiedad, index) in objetoFruta" :key="value">{{ index }} - {{ propiedad }}: {{ value }}</li>
</ul>

</template>

<style>
ul{
    list-style-type: none;
    color: aquamarine;
}

</style>

