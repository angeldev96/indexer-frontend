<template>
    <div class="p-4">
      <div class="flex items-center">
        <input 
          v-model="keyword" 
          placeholder="Buscar palabra clave..." 
          class="p-2 border rounded mr-2 flex-grow"
        />
        <button @click="searchEmails" class="bg-blue-500 text-white p-2 rounded hover:bg-blue-600">
          Search
        </button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        keyword: ''
      };
    },
    methods: {
      searchEmails() {
        // Aquí es donde harías la llamada a la API en el futuro
        console.log("Buscando:", this.keyword);
      }
    }
  };
  </script>
  