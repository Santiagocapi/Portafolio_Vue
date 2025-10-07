<script setup>
import Education from './components/Education.vue'
import NavBar from './components/Navbar.vue'
import Profile from './components/Profile.vue'
</script>

<template>
  <!-- HTML Content with vue's tools -->
  <header>
    <!-- NavBar Component -->
    <NavBar />
  </header>
  <section>
    <!-- Profile Component -->
    <Profile />
  </section>
  <main>
    <!-- Education Component -->
    <Education />
  </main>
</template>

<style scoped></style>
