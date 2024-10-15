<script setup>
import BackToTop from '../components/BackToTop.vue'
</script>

<template>
  <main class="home-page">
      <!-- Section de présentation -->
    <section class="intro">
      <h1>Kacper Szymanski</h1>
      <p>Étudiant en Web Design</p>
      <p>Bienvenue sur mon portfolio !</p>
      <a href="/projets" class="btn">Voir mes projets</a>
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
      <div class="projects-list">
        <article class="project-item">
          <h2>Maquette site fictif - XUI </h2>
          <a href="/projets" class="btn">Voir plus</a>
        </article>
        <!-- 
        <article class="project-item">
          <h2>Projet 2</h2>
          <a href="/projets" class="btn">Voir plus</a>
        </article>
      -->
      </div>
    </section>

    <section class="github" id="github">
      <h2>GitHub</h2>
      <p>Vous pouvez consulter un premier jet de mon CV et de mon Portfolio mais également mes premiers exercices en JavaScript. <br>
        Cela se passe ici: <a href="https://github.com/Kvcpi" target="_blank">www.github.com/Kvcpi</a>
      </p>
    </section>

    <!-- Section contact -->
    <section class="contact" id="contact">
      <h2>Contactez-moi</h2>
      <p>Envie de collaborer ou d'en savoir plus ?</p>
      <RouterLink to="/contact" id="transition-link" class="btn">Me Contacter</RouterLink>
    </section>
  </main>
  <BackToTop />
</template>


