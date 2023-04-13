<script setup>
    const arrayFrutas = [
        {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
            stock: 0,
        },
        {
            name: "Pera",
            price: "$2.00",
            description: "Una pera",
            stock: 10,
        },
        {
            name: "Naranja",
            price: "$3.00",
            description: "Una naranja",
            stock: 20,
        },
    ];

</script>


<template>

<ul>
    <!-- el vfor se usa en el template que no se muestra en el DOM osea es imvisible, pero funciona para pasar el item al vif -->
    <template v-for="item in arrayFrutas" :key="name">
        <li v-if="item.stock > 0">{{ item.name }} - {{ item.price }} - {{ item.stock }}</li>
    </template>
</ul>

</template>