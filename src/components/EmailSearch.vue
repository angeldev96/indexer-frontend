<template>
    <div class="p-4 relative">
      <div class="flex items-center border rounded">
        <!-- Ícono de lupa -->
        <svg class="w-6 h-6 ml-2 text-gray-500" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth="2" d="M21 21l-6-6m2-6a7 7 0 11-14 0 7 7 0 0114 0z" />
        </svg>
  
        <input 
          v-model="keyword" 
          placeholder="Buscar palabra clave..." 
          class="p-2 flex-grow border-none outline-none"
        />
  
        <!-- Ícono de filtro -->
        <svg @click="showFilters = !showFilters" class="w-6 h-6 mr-2 text-gray-500 cursor-pointer" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path strokeLinecap="round" strokeLinejoin="round" strokeWidth="2" d="M3 3v3a1 1 0 001 1h16a1 1 0 001-1V3M3 10v3a1 1 0 001 1h16a1 1 0 001-1v-3M3 17v3a1 1 0 001 1h16a1 1 0 001-1v-3" />
        </svg>
      </div>
      <button @click="searchEmails" class="mt-2 bg-blue-500 text-white p-2 rounded hover:bg-blue-600">
        Search
      </button>
  
      <!-- Cuadro de filtros -->
      <div v-if="showFilters" class="absolute top-full mt-2 w-64 bg-white border rounded shadow-lg p-4">
        <div class="mb-2">
          <label class="block text-sm font-bold mb-1">De:</label>
          <input v-model="filterFrom" class="w-full p-2 border rounded" />
        </div>
        <div class="mb-2">
          <label class="block text-sm font-bold mb-1">Para:</label>
          <input v-model="filterTo" class="w-full p-2 border rounded" />
        </div>
        <div class="mb-2">
          <label class="block text-sm font-bold mb-1">Asunto:</label>
          <input v-model="filterSubject" class="w-full p-2 border rounded" />
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        keyword: '',
        showFilters: false,
        filterFrom: '',
        filterTo: '',
        filterSubject: ''
      };
    },
    methods: {
      searchEmails() {
        // Aquí es donde harías la llamada a la API en el futuro
        console.log("Buscando:", this.keyword);
        console.log("Filtros - De:", this.filterFrom, "Para:", this.filterTo, "Asunto:", this.filterSubject);
      }
    }
  };
  </script>
  