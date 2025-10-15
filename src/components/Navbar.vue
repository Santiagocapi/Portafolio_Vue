<template>
  <nav class="navbar">
    <h3>Portafolio Personal</h3>
    <div class="navegation">
      <a v-for="item in navegation" :key="item.id" :href="item.link">{{ item.name }}</a>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
const navegation = ref([
  { id: 1, name: 'Proyectos', link: '#project' },
  { id: 2, name: 'Contacto', link: '#contact' },
])
</script>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 10%;
  border-bottom: 1px solid var(--grey);

  h3 {
    color: var(--primary);
  }

  .navegation {
    display: flex;
    gap: 20px;
  }
}

.navegation a {
  color: var(--text-primary);
  font-weight: 500;
  transition: color 0.3s ease;

  &:hover {
    color: var(--accent);
  }
}
</style>
