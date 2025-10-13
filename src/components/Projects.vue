<template>
  <section id="project" class="projects-section">
    <h2>Mis Proyectos</h2>
    <div class="projects-grid">
      <article v-for="project in projects" :key="project.id" class="project-card">
        <div class="card-image-container">
          <img :src="project.image" :alt="'Imagen del proyecto ' + project.title" />
        </div>
        <div class="card-content">
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <div class="project-tags">
            <span v-for="tag in project.tags" :key="tag">{{ tag }}</span>
          </div>
          <div class="project-link">
            <a :href="project.repoUrl" target="_blank" class="btn btn-secondary">Ver Código</a>
          </div>
        </div>
      </article>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const projects = ref([
  {
    id: 1,
    title: 'Nombre del Proyecto 1',
    image: '',
    description: 'Breve descripción del proyecto.',
    tags: [' Unity', 'C#'],
    repoUrl: '#',
  },
  {
    id: 2,
    title: 'Nombre del Proyecto 2',
    image: '',
    description: 'Breve descripción del proyecto.',
    tags: ['JavaScript', 'Nodejs', 'HTML', 'CSS'],
    repoUrl: '#',
  },
  {
    id: 3,
    title: 'Nombre del Proyecto 3',
    image: '',
    description: 'Breve descripción del proyecto.',
    tags: ['Python', 'Django'],
    repoUrl: '#',
  },
])
</script>

<style scoped>
.projects-section {
  padding: 4rem 2rem;
  background-color: var(--light-grey);
}

h2 {
  text-align: center;
  color: var(--primary);
  font-size: 2rem;
  margin-bottom: 3rem;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}
.project-card {
  background: var(--white);
  border-radius: 12px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
}
.project-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.12);
}
.card-image-container {
  overflow: hidden;
  height: 200px;
}
.card-image-container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.4s ease;
}
.project-card:hover img {
  transform: scale(1.05);
}
.card-content {
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}
.card-content h3 {
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
}
.card-content p {
  font-size: 0.95rem;
  color: var(--text-secondary);
  line-height: 1.6;
  flex-grow: 1;
}
.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin: 1rem 0;
}
.project-tags span {
  background-color: #e9ecef;
  color: var(--text-secondary);
  padding: 0.25rem 0.75rem;
  border-radius: 999px;
  font-size: 0.8rem;
}
.project-links {
  display: flex;
  gap: 1rem;
  margin-top: auto;
}
.btn {
  padding: 0.6rem 1.2rem;
  border-radius: 8px;
  text-align: center;
  font-weight: 500;
  transition: all 0.3s ease;
}
.btn-primary {
  background-color: var(--primary);
  color: var(--white);
}
.btn-primary:hover {
  background-color: #0b5ed7;
}
.btn-secondary {
  background-color: transparent;
  color: var(--primary);
  border: 1px solid var(--primary);
}
.btn-secondary:hover {
  background-color: var(--primary);
  color: var(--white);
}
</style>
