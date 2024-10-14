<template>
    <a href="#" class="scroll-to-top" aria-label="Retour en haut" @click.prevent="scrollToTop">
      <i class="fas fa-arrow-up"></i> <!-- Utilise Font Awesome pour l'icône -->
    </a>
  </template>
  
  <script>
  export default {
    name: 'ScrollToTop',
    mounted() {
      window.addEventListener('scroll', this.toggleButton);
    },
    beforeDestroy() {
      window.removeEventListener('scroll', this.toggleButton);
    },
    methods: {
      toggleButton() {
        const scrollToTopBtn = this.$el;
        if (document.body.scrollTop > 200 || document.documentElement.scrollTop > 200) {
          scrollToTopBtn.style.display = "block"; // Affiche la flèche
        } else {
          scrollToTopBtn.style.display = "none"; // Cache la flèche
        }
      },
      scrollToTop() {
        window.scrollTo({
          top: 0,
          behavior: 'smooth' // Défilement en douceur
        });
      }
    }
  }
  </script>
  
  <style scoped>
  .scroll-to-top {
    position: fixed;
    bottom: 30px; /* Ajuste la position selon tes préférences */
    right: 30px; /* Ajuste la position selon tes préférences */
    background-color: #ff9800; /* Couleur de fond de la flèche */
    color: white; /* Couleur de l'icône */
    border-radius: 50%;
    padding: 15px;
    text-align: center;
    font-size: 24px; /* Ajuste la taille de l'icône */
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    transition: background-color 0.3s ease, transform 0.3s ease;
    z-index: 1000; /* S'assurer que la flèche est au-dessus des autres éléments */
    display: none; /* Masquer par défaut */
  }
  
  .scroll-to-top:hover {
    background-color: #e68a00; /* Couleur au survol */
    transform: scale(1.1); /* Effet de zoom au survol */
  }
  </style>
  