<template>
  <section class="profile">
    <div class="profile_content">
      <div class="img_container">
        <img src="../static/img/IMG-20250115-WA0221.jpg" alt="" />
      </div>
      <div class="profile_text">
        <h1>Hola, Soy <span class="text_highlight">Santiago Capitani</span></h1>
        <h4>Técnico Informático y desarrollador Full Stack</h4>
        <p>
          Me especializo en crear soluciones web completas, desde el diseño del frontend hasta la
          lógica del backend. Me apasiona aprender nuevas tecnologías y construir proyectos que unan
          funcionalidad y diseño.
        </p>
        <div class="social_network"></div>
      </div>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.profile {
  padding: 30px 30rem;
  display: flex;
  justify-content: center;
}

.profile_content {
  display: flex;
  align-items: center;
  gap: 50px;
}

.img_container {
  display: inline-block;
  border: 4px solid var(--green);
  padding: 6px;
  background-color: #fff;
}

img {
  display: block;
  width: 300px;
  height: 350px;
}

.profile_text {
  max-width: 600px;
  display: flex;
  flex-direction: column;
  gap: 15px;
}

h1 {
  font-size: 2.5rem;
}

.text_highlight {
  color: var(--dark_blue);
}

h4 {
  font-size: 1rem;
  color: var(--grey);
}
</style>
