<template>
  <main class="projects-page">
    <section class="intro">
      <h1>Mes Projets</h1>
      <p>Découvrez une sélection de mes travaux récents</p>
    </section>

    <section class="projects-list">
      <article class="project-item" v-for="project in projects" :key="project.id">
        <h2>{{ project.title }}</h2>
        <p>{{ project.description }}</p>
        <div class="project-tags">
          <span v-for="tag in project.tags" :key="tag">{{ tag }}</span>
        </div>
        <a :href="project.link" class="btn" target="_blank">Voir le projet</a>
      </article>
    </section>
  </main>
  <BackToTop />
</template>

<script setup>
import { ref } from 'vue'

const projects = ref([
  {
    id: 1,
    title: 'Maquette site fictif - XUI',
    description: 'Maquette du site web fictif sous le nom de Sweet Home.',
    tags: ['Figma', 'Illustrator', 'Photoshop',],
    link: './src/img/Sweet Home - maquettes.png',
  },
  {
    id: 2,
    title: 'Application de gestion de tâches',
    description: 'Une application web permettant aux utilisateurs de gérer leurs tâches quotidiennes, avec des fonctionnalités de tri et de filtrage.',
    image: '/path/to/project2-image.jpg',
    tags: ['JavaScript', 'HTML5', 'LocalStorage'],
    link: '#'
  },
  // Ajoutez d'autres projets ici
])
import BackToTop from '../components/BackToTop.vue'
</script>