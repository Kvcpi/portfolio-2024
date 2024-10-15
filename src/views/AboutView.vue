<template>
  <main class="about-page">
    <section class="intro">
      <h1>À propos de moi</h1>
    </section>

    <section class="about-content" data-aos="fade-up">
      <div class="about-text" data-aos="fade-right" data-aos-duration="800">
        <h2>Qui suis-je ?</h2>
        <p>
          Je suis Kacper Szymanski, un étudiant en Web Design passionné par la création d'expériences numériques
          uniques et engageantes. Mon parcours dans le monde du design et du développement web a commencé il y a moins
          de 2 ans, et depuis, je n'ai cessé d'apprendre et de grandir dans ce domaine en constante évolution.
        </p>
        <p>
          Ma formation en Web Design m'a donné une base solide en design graphique et en programmation, que j'ai
          constamment enrichie par des projets personnels et des collaborations diverses.
        </p>
        <p>
          Je possède également un permis de conduire, ce qui me permet de me déplacer facilement pour des rendez-vous ou des missions sur site.
        </p>
      </div>
      
      <div class="about-skills" data-aos="fade-left" data-aos-duration="800">
        <h2>Mes compétences</h2>
        <ul>
          <li>HTML5 / CSS3 / JavaScript</li>
          <li>Responsive Web Design</li>
          <li>UI/UX Design</li>
          <li>WordPress & WooCommerce</li>
          <li>Adobe Suite (Photoshop, Illustrator)</li>
        </ul>
      </div>

      <div class="about-skills" data-aos="fade-left" data-aos-duration="800" data-aos-delay="200">
        <h2>Mes qualités</h2>
        <ul>
          <li>Précrastinateur</li>
          <li>Capacité d'écoute</li>
          <li>Adaptation</li>
          <li>Débrouillard</li>
        </ul>
      </div>
    </section>

    <section id="experiences-professionnelles" data-aos="fade-up">
      <h2>Mes Expériences Professionnelles</h2>
      <div class="experience-card" data-aos="fade-right" data-aos-duration="800">
        <h3>mars 2023 - présent</h3>
        <h4>Job étudiant</h4>
        <p>Colruyt, Etterbeek</p>
        <p>Employé polyvalent en temps qu'étudiant dans un magasin. (caisse, stock, magasin, frigo)</p>
      </div>

      <div class="experience-card" data-aos="fade-right" data-aos-duration="800" data-aos-delay="200">
        <h3>février 2023 - mars 2023</h3>
        <h4>Stage Secrétariat</h4>
        <p>Facq, Zaventem</p>
        <p>Gestion des ressources humaines</p>
      </div>

      <div class="experience-card" data-aos="fade-right" data-aos-duration="800" data-aos-delay="400">
        <h3>2022</h3>
        <h4>Stage Secrétariat</h4>
        <p>Bruxelles Formation, Uccle</p>
        <p>Gestion de contrat, de planning et participation aux réunions d'équipe.</p>
      </div>
    </section>

    <section id="parcours-scolaire" data-aos="fade-up">
      <h2>Mon Parcours Scolaire</h2>
      <div class="timeline">
        <div class="timeline-item" data-aos="fade-up" data-aos-duration="800">
          <div class="timeline-content">
            <h3>2023 - Présent</h3>
            <h4>BES en Web Design</h4>
            <p>IFOSUP, Wavre</p>
            <p>Actuellement en 2e année, je développe mes compétences en design web, UI/UX et développement front-end
              avec des technologies modernes comme Vue.js et Vite.</p>
          </div>
        </div>

        <div class="timeline-item" data-aos="fade-up" data-aos-duration="800" data-aos-delay="200">
          <div class="timeline-content">
            <h3>2021 - 2023</h3>
            <h4>CESS-CQ6 (Option Bureautique)</h4>
            <p>Athénée Royal Jean Absil, Etterbeek</p>
            <p>Obtention de mon CESS et d'un diplôme technique en tant que Technicien de bureau.
              J'ai développé de solides compétences en bureautique comme le pack Office (Word, Excel, PowerPoint), la
              dactylographie, la gestion des documents et bien plus encore.
            </p>
          </div>
        </div>
      </div>
    </section>

    <section class="cta" data-aos="fade-up">
      <h2>Envie de travailler ensemble ?</h2>
      <RouterLink to="/contact" class="btn">Contactez-moi</RouterLink>
    </section>
  </main>
  <BackToTop />
</template>

<script setup>
import BackToTop from '../components/BackToTop.vue'
</script>
