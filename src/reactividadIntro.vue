<script setup>
import { ref } from 'vue';

const name = "Intro Reactividad";
const counter = ref(0);

const increment = () => counter.value++;
const decrement = () => counter.value--;
const resert = () => counter.value = 0;



</script>

<template>

<h1> Vue {{ name }}</h1>

<h2 v-if="counter < 0" :style="`color:red`">{{ counter }}</h2>
<h2 v-else-if="counter >= 10" :style="`color: green`">{{ counter }}</h2>
<h2 v-else>{{ counter }}</h2>


<button v-on:click="increment">Aumentar</button>
<button v-on:click="decrement">Reducir</button>
<button v-on:click="resert">Resetear</button>

</template>

