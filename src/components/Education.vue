<template>
  <section class="education_content">
    <h2>Mi Educación</h2>
  </section>
</template>

<script setup>
const props = defineProps({
  education: {
    type: Array,
    default: () => [
      {
        id: 1,
        degree: 'Tecnico Informatico',
        institution: 'Escuela Técnica de la Universidad de Mendoza',
        years: '2018-2023',
        start: 2018,
        end: 2023,
      },
      {
        id: 2,
        degree: 'Ingeniero Informático',
        institution: 'Universidad de Mendoza',
        years: '2024-2025',
        start: 2024,
        end: 2025,
      },
      {
        id: 3,
        degree: 'Tecnico en Programación',
        institution: 'Universidad Tecnológica Nacional',
        years: '2025-Actualidad',
        start: 2025,
        end: 'Actualidad',
      },
    ],
  },
})
</script>

<style scoped></style>
