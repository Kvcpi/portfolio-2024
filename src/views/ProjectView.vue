<template>
  <main class="projects-page">
    <section class="intro">
      <h1>Mes Projets</h1>
      <p>Découvrez une sélection de mes travaux récents</p>
    </section>

    <section class="projects-list">
      <article class="project-item" v-for="project in projects" :key="project.id">
        <img :src="project.image" :alt="project.title">
        <h2>{{ project.title }}</h2>
        <p>{{ project.description }}</p>
        <div class="project-tags">
          <span v-for="tag in project.tags" :key="tag">{{ tag }}</span>
        </div>
        <a :href="project.link" class="btn" target="_blank">Voir le projet</a>
      </article>
    </section>
  </main>
</template>

<script setup>
import { ref } from 'vue'

const projects = ref([
  {
    id: 1,
    title: 'Site e-commerce responsif',
    description: 'Un site e-commerce moderne et entièrement responsif, développé avec Vue.js et intégré à une API REST.',
    image: '/path/to/project1-image.jpg',
    tags: ['Vue.js', 'CSS3', 'API REST'],
    link: '#'
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
</script>

<style scoped>
.projects-page {
  padding-top: 80px;
}

.projects-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  padding: 60px 20px;
  background-color: var(--secondary-color);
}

.project-item {
  background-color: var(--background-color);
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease-in-out;
}

.project-item:hover {
  transform: translateY(-10px);
}

.project-item img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.project-item h2 {
  font-size: 1.5em;
  margin: 15px;
}

.project-item p {
  margin: 0 15px 15px;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  margin: 0 15px 15px;
}

.project-tags span {
  background-color: var(--accent-color);
  color: var(--primary-color);
  padding: 5px 10px;
  margin-right: 5px;
  margin-bottom: 5px;
  border-radius: 15px;
  font-size: 0.8em;
}

.project-item .btn {
  display: block;
  margin: 15px;
  text-align: center;
}

@media screen and (max-width: 768px) {
  .projects-list {
    grid-template-columns: 1fr;
  }
}
</style>