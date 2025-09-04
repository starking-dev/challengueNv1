<!-- Puedes agregar esto en App.vue o crear un nuevo archivo, por ejemplo, AddList.vue -->
<template>
    <div id="addEle" class="bg-teal-200" >

    
  <div class="left-0 p-5 w-full bg-sky-800 text-white shadow-lg rounded-xl mb-8" style="margin-top: 20px; margin-bottom: 20px;">
    <form @submit.prevent="addItem" class="flex gap-2">
      <input
        v-model="newItem"
        type="text"
        placeholder="Agrega una nueva idea"
        class="flex-1 border rounded px-2 py-1 text-black bg-teal-200"
      />
      <button type="submit" class="bg-blue-500 text-white px-4 py-1 rounded">
        Agregar
      </button>
    </form>
    <ul class="mt-4">
      <li v-for="(item, index) in items" :key="index" class="py-1 border-b">
        {{ item }}
      </li>
    </ul>
  </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const newItem = ref('')
const items = ref([])

function addItem() {
  if (newItem.value.trim()) {
    items.value.push(newItem.value.trim())
    newItem.value = ''
  }
}
</script>

<style scoped>
/* Opcional: estilos para mejorar la apariencia */
</style>