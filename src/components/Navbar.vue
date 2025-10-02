<template>
  <nav class="navbar">
    <h3>Portafolio Personal</h3>

    <!-- Navegation Links -->
    <div class="navegation">
      <a v-for="item in navegation" :key="item.id" :href="item.link">{{ item.name }}</a>
    </div>

    <!-- Language Selection -->
    <div class="box_lang_selector" @click="toggleMenu">
      <img src="../static/img/language-svgrepo-com.svg" alt="" />
      <ul v-if="showMenu" class="lang_menu">
        <li @click="setLanguage('es')">Español</li>
        <li @click="setLanguage('en')">English</li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px 10px 20px;
  border-bottom: 1px solid #ddd;
}

nav h3 {
  color: var(--dark-blue);
}

.box_lang_selector {
  position: relative;
  border: 2px solid;
  border-radius: 5px;
  background-color: var(white);
}

.box_lang_selector:hover {
  transition: 0.5s;
  background-color: var(--green);
}

img {
  width: 35px;
  cursor: pointer;
  margin-top: 3px;
}

.navegation {
  display: flex;
  gap: 20px;
  margin-right: 35px;
}

.navegation a {
  color: black;
  font-weight: 500;
}

.navegation a:hover {
  transition: 0.5s;
  color: var(--dark-blue);
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

<script setup>
import '../static/css/styles.css' // Importar estilos globales
import { ref } from 'vue' // Importar ref para crear referencias reactivas

const navegation = ref([
  { id: 1, name: 'Educacion', link: '#education' },
  { id: 2, name: 'Proyectos', link: '#project' },
  { id: 3, name: 'Contacto', link: '#contact' },
])

// Show language menu
const showMenu = ref(false)
const currentLanguage = ref('es')

function toogleMenu() {
  showMenu.value = !showMenu.value
}

function setLanguage(lang) {
  currentLanguage.value = lang
  showMenu.value = false

  // Seeing whether to change the language manually
  // or use the internationalization library called vue-i18n,
  // with that I can have a translation file in a JSON
}
</script>
