<script setup>
  const name = "Vue Dinamico";
  //eñ estudo usando v-bind
  const styleColor = "color: royalblue";
  const arrayColores = ["red","cyan","yellow", "black", "orange"];
  const activo = false;
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <h2>{{ arrayColores }}</h2>
  <h2 :style="`color: ${arrayColores[2]}`">color de arrayColores</h2>
  <h2>
    {{ activo ? "Estoy Activo" : "Estoy Inactivo" }}
  </h2>
  <p  v-if="activo">este es sucnado esta actrivo</p>
  <p v-else>este  p  es cuando no no activo</p>

  <ul>
    <li v-for="(color, index) in arrayColores" :key="index">{{ index }} - {{ color }}</li>
  </ul>
</template>

<style>
h1{
  color: aqua;

}</style>