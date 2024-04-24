<template>
  <div>
    <h2>Lista De Tareas</h2>
    <input type="text" v-model = "nuevaTarea" @keyup.enter="addTarea">
    <ul>
      <li v-for= "(tarea, index) in tareas" :key="index">
               {{ tarea }}
      </li>
      
    </ul>
  </div>
</template>


<script setup

import { ref } from 'vue';
// Importa la función ref de Vue REACTIVIDAD

const tareas = ref([]);
// Crea una referencia reactiva llamada "tareas" con un array vacío como valor inicial

const nuevaTarea = ref('');
// Crea una referencia reactiva llamada "nuevaTarea" con una cadena vacía como valor inicial

const addTarea = () => {
  tareas.value.push(nuevaTarea.value);
  // Agrega la nueva tarea al array de tareas
  nuevaTarea.value = '';
  // Limpia la nueva tarea
}

</script>


<style> </style>
