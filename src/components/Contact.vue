<template>
  <section class="contact-section" id="contact">
    <h2>Contacto</h2>
    <!-- Agrego boton para descargar cv en profile.vue
          Algunos cambios en los tags en las cards de projects.vue y education.vue
          Habilito link de linkedin en profile.vue
          Cambios en el codigo de css, mas estructurado
          -->
    <p class="subtitle">¿Tienes una pregunta o quieres trabajar juntos? Déjame un mensaje.</p>
    <div class="form-card">
      <form @submit.prevent="handleSubmit">
        <div class="input-group">
          <label for="name">Nombre</label>
          <input type="text" id="name" placeholder="Nombre" v-model="form.name" required />
        </div>
        <div class="input-group">
          <label for="email">Email</label>
          <input type="email" id="email" placeholder="Gmail" v-model="form.email" required />
        </div>
        <div class="input-group">
          <label for="message">Mensaje</label>
          <textarea id="message" placeholder="Mensaje" v-model="form.message" required></textarea>
        </div>
        <button type="submit" class="btn submit-btn">Enviar Mensaje</button>
      </form>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  message: '',
})

const handleSubmit = () => {
  // Aca iría la lógica para enviar el formulario.
  console.log('Formulario enviado:', form.value)
  alert('¡Mensaje enviado con éxito!')
  // Resetear formulario
  form.value = { name: '', email: '', message: '' }
}
</script>

<style scoped>
.contact-section {
  padding: 4rem 2rem;
  text-align: center;

  .subtitle {
    color: var(--text-secondary);
    margin-bottom: 3rem;
    max-width: 500px;
    margin-left: auto;
    margin-right: auto;
  }

  .form-card {
    max-width: 700px;
    margin: 0 auto;
    background-color: var(--white);
    padding: 2.5rem;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  }
}

.input-group {
  text-align: left;
  margin-bottom: 1.5rem;

  label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: 500;
    color: var(--text-primary);
  }

  input,
  textarea {
    width: 100%;
    padding: 0.8rem 1rem;
    border-radius: 8px;
    border: 1px solid var(--grey);
    font-size: 1rem;
    transition:
      border-color 0.3s,
      box-shadow 0.3s;
  }
}

.submit-btn {
  background-color: transparent;
  color: var(--primary);
  font-weight: 800;
  border: 2px solid var(--primary);

  &:hover {
    background-color: var(--primary);
    color: var(--white);
  }
}
</style>
