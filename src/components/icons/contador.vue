<template>
  <!-- Estructura visual del componente -->
  <h1>Hello Jurgen</h1>
  <p>{{ contador }}</p>
  <button @click="incrementar">Incrementar</button>
  <button @click="decrementar">Decrementar</button>
</template>

<script setup>
import { ref } from "vue";

// Definición de variables y funciones
const contador = ref(0); // Variable reactiva que almacena el contador
const incrementar = () => {
  contador.value += 7; // Función para incrementar el contador en 7
};

const decrementar = () => {
  contador.value -= 7; // Función para decrementar el contador en 7
};
</script>

<style scoped>
p {
  color: rgb(89, 208, 226);
}
</style>
