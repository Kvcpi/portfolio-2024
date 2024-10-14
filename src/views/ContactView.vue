<template>
  <main class="contact-page">
    <section class="intro">
      <h1>Contactez-moi</h1>
      <p>N'hésitez pas à me contacter pour toute question ou proposition de collaboration</p>
    </section>

    <section class="contact-form">
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Nom</label>
          <input type="text" id="name" v-model="form.name" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="form.email" required>
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" v-model="form.message" required></textarea>
        </div>
        <button type="submit" class="btn">Envoyer</button>
      </form>
    </section>

    <section class="contact-info">
      <h2>Autres moyens de me contacter</h2>
      <ul>
        <li>Email : <a href="mailto:kacperszymanski.design@gmail.com">kacperszymanski.design@gmail.com</a></li>
        <li>Téléphone : <a href="tel:+32488063799">+32 488 063 799</a></li>
      </ul>
    </section>
  </main>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  message: ''
})

const submitForm = () => {
  // Ici, vous pouvez ajouter la logique pour envoyer le formulaire
  console.log('Formulaire soumis', form.value)
  // Réinitialiser le formulaire après soumission
  form.value = { name: '', email: '', message: '' }
}
</script>

<style scoped>
.contact-page {
  padding-top: 80px;
}

.contact-form, .contact-info {
  padding: 60px 20px;
  background-color: var(--secondary-color);
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  margin-bottom: 5px;
  font-weight: 500;
}

input, textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 5px;
}

textarea {
  height: 150px;
}

.contact-info ul {
  list-style-type: none;
  padding: 0;
}

.contact-info li {
  margin-bottom: 10px;
}

@media screen and (max-width: 768px) {
  .contact-form, .contact-info {
    padding: 40px 20px;
  }
}
</style>