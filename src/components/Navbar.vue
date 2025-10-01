<template>
  <nav class="navbar">
    <h2>Portafolio Personal</h2>

    <div class="navegation">
      <a v-for="item in navegation" :key="item.id" :href="item.link">{{ item.name }}</a>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue' // Importar ref para crear referencias reactivas
const navegation = ref([
  { id: 1, name: 'Educacion', link: '#education' },
  { id: 2, name: 'Proyectos', link: '#project' },
  { id: 3, name: 'Contacto', link: '#contact' },
])
</script>

<style scoped>
* {
  text-decoration: none;
}
</style>
