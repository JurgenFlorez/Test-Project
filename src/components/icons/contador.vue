<template>
  <!-- Estructura visual del componente -->
  <h1 class="Title">Hello</h1>
  <h1 class="Name">Jurgen</h1>
  <p>{{ contador }}</p>
  <button class="boton1" @click="incrementar">Incrementar</button>
  <button class="boton2" @click="decrementar">Decrementar</button>
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
/* Estilos del componente */

p {
  color: rgb(68, 251, 229);
  font-weight: bold;
}
.Title {
  color: #da0396;
  text-shadow: 2px 2px 4px rgb(255, 226, 251);
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}

.Name {
  color: white;
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  text-shadow: 2px 2px 4px rgba(255, 255, 255, 0.5);
}
.Title,
.Name {
  display: inline; /* Mostrar en línea */
  /* Opcionalmente, puedes agregar un margen entre los elementos para separarlos */
  margin-right: 20px; /* Por ejemplo, un margen de 20 píxeles */
}

.boton1 {
  padding: 10px 20px; /* Añade relleno interno al botón */
  background-color: #03da1c; /* Establece el color de fondo */
  color: white; /* Establece el color del texto */
  border: none; /* Quita el borde del botón */
  cursor: pointer; /* Cambia el cursor al pasar por encima */
  border-radius: 5px; /* Agrega bordes redondeados */
  margin-right: 10px; /* Añade margen a la derecha para separar los botones */
  font-weight: bold;
}

.boton2 {
  padding: 10px 20px; /* Añade relleno interno al botón */
  background-color: #da0396; /* Establece el color de fondo */
  color: white; /* Establece el color del texto */
  border: none; /* Quita el borde del botón */
  cursor: pointer; /* Cambia el cursor al pasar por encima */
  border-radius: 5px; /* Agrega bordes redondeados */
  margin-right: 10px; /* Añade margen a la derecha para separar los botones */
  font-weight: bold;
}
</style>
