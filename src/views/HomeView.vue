<script setup>
</script>

<template>
  <main class="home-page">
      <!-- Section de présentation -->
    <section class="intro">
      <h1>Kacper Szymanski</h1>
      <p>Étudiant en Web Design</p>
      <p>Bienvenue sur mon portfolio !</p>
      <a href="#projects" class="btn">Voir mes projets</a>
    </section>

    <!-- Section compétences -->
    <section class="skills" id="skills">
      <h2>Compétences</h2>
      <ul>
        <li>HTML / CSS / JavaScript</li>
        <li>Suite Adobe (Photoshop, Illustrator)</li>
        <li>WordPress & WooCommerce</li>
        <li>Responsive Design</li>
      </ul>
    </section>

    <!-- Section projets -->
    <section class="projects" id="projects">
      <h2>Mes Projets</h2>
      <div class="project-list">
        <article class="project-item">
          <h3>Projet 1</h3>
          <p>Description du projet 1</p>
          <a href="#" class="btn">Voir plus</a>
        </article>
        <article class="project-item">
          <h3>Projet 2</h3>
          <p>Description du projet 2</p>
          <a href="#" class="btn">Voir plus</a>
        </article>
      </div>
    </section>

    <!-- Section contact -->
    <section class="contact" id="contact">
      <h2>Contactez-moi</h2>
      <p>Envie de collaborer ou d'en savoir plus ?</p>
      <RouterLink to="/contact" class="btn">Me Contacter</RouterLink>
    </section>
  </main>
</template>


