<script setup>
    const name = "Vue Dinamico"

    //metodo
    const handleClick = (message) => console.log(message);
    
</script>


<template>
    <h1> Hola {{ name.toUpperCase() }}</h1>
    <button v-on:click.right.prevent="handleClick('activo con b-derecho')">Activame derecho</button>
    <button @:click.middle="handleClick('activo con b-medio')">Activame medio</button>
    <button @:click.left="handleClick('Activo con b-izquierdo')">Activame izquierdo</button>
</template>