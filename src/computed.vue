<script setup>
import { ref, computed } from 'vue';

const name = "Intro Reactividad";
const counter = ref(0);
const numerosFavoritos = ref([]);

const classCounter = computed(() => {
    if (counter.value < 0) {
        return 'negative'
    }
    if (counter.value >= 10) {
        return 'positive'
    }else{
        return ''
    }
});

const numeroRepetido = computed(() =>{
   return (numerosFavoritos.value.includes(counter.value))
})



const increment = () => counter.value++;
const decrement = () => counter.value--;
const resert = () => counter.value = 0;
const addNumber = () => numerosFavoritos.value.push(counter.value);
</script>

<template>
<div class="container text-center mt-3">
    <h1> Vue {{ name }}</h1>

    <h2 :class="classCounter">{{ counter }}</h2>

    <div class="btn-group">
        <button class="btn btn-success" v-on:click="increment">Aumentar</button>
        <button class="btn btn-danger" v-on:click="decrement">Reducir</button>
        <button class="btn btn-secondary" @:click="resert">Resetear</button>
        <button class="btn btn-primary" @:click="addNumber" :disabled="numeroRepetido">Add</button>
    </div>
    <p>Numeros Favoritos</p>
    <ul class="list-group">
        <li class="list-group-item" v-for="numero in numerosFavoritos" :key="numero">{{ numero }}</li>
    </ul>
</div>
</template>


<style>
h1{
    color: darkcyan;
}
.negative{
    color: red;
}
.positive{
    color: green;
}
</style>

