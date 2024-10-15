<script setup>
import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>

<template>
  <header :class="{ 'menu-open': isMenuOpen }">
    <div class="wrapper">
      <nav>
        <RouterLink to="/" class="logo" @click="closeMenu"><img src="/src/img/logo2.png" alt="logo"></RouterLink>
        <div class="nav-links" :class="{ 'active': isMenuOpen }">
          <RouterLink to="/" @click="closeMenu">Home</RouterLink>
          <RouterLink to="/projets" @click="closeMenu">Mes Projets</RouterLink>
          <RouterLink to="/about" @click="closeMenu">À propos</RouterLink>
          <RouterLink to="/contact" @click="closeMenu">Contact</RouterLink>
        </div>
        <div class="hamburger" @click="toggleMenu">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </nav>
    </div>
  </header>
  <main>
    <RouterView />
  </main>
</template>