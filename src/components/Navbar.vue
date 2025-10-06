<template>
  <nav class="navbar">
    <h3>Portafolio Personal</h3>

    <!-- Navegation Links -->
    <div class="navegation">
      <a v-for="item in navegation" :key="item.id" :href="item.link">{{ item.name }}</a>
    </div>
  </nav>
</template>

<script setup>
import '../static/css/styles.css' // Importar estilos globales
import { ref } from 'vue' // Importar ref para crear referencias reactivas

const navegation = ref([
  { id: 1, name: 'Educacion', link: '#education' },
  { id: 2, name: 'Proyectos', link: '#project' },
  { id: 3, name: 'Contacto', link: '#contact' },
])
</script>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 20px 15px 20px;
  border-bottom: 1px solid #ddd;
}

nav h3 {
  color: var(--dark_blue);
}

.navegation {
  display: flex;
  gap: 20px;
}

.navegation a {
  color: black;
  font-weight: 500;
}

.navegation a:hover {
  transition: 0.5s;
  color: var(--green);
}

.lang_menu {
  position: absolute;
  top: 32px;
  right: 0;
  background: white;
  border: 1px solid #ddd;
  border-radius: 5px;
  list-style: none;
  padding: 0.5rem 0;
  width: 120px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.lang_menu li {
  padding: 0.5rem 1rem;
  cursor: pointer;
}

.lang-menu li:hover {
  background: var(--dark-blue);
  color: white;
}
</style>
