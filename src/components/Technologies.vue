<template>
  <section class="technologies">
    <h2>Mis Tecnologías</h2>
    <div v-for="category in techCategories" :key="category.name" class="category-block">
      <h3>{{ category.name }}</h3>
      <div class="pills-container">
        <span v-for="tech in category.items" :key="tech" class="pill">
          {{ tech }}
        </span>
      </div>
    </div>
  </section>
</template>
