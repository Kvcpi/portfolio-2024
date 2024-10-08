<script setup>
import { RouterLink, RouterView } from 'vue-router'
import './assets/main.css';
</script>

<template>
  <header class="fixed-header"> 
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/projets">Mes Projets</RouterLink>
        <RouterLink to="/about">À propos</RouterLink>
        <RouterLink to="/contact">Contact</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>
