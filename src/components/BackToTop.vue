<!-- BackToTop.vue -->
<template>
    <button 
    v-if="showBackToTop" 
    @click="scrollToTop" 
    class="back-to-top" 
    :class="{ show: showBackToTop }" 
  >
    ↑
  </button>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  
  const showBackToTop = ref(false);
  
  const handleScroll = () => {
    showBackToTop.value = window.scrollY > 300;
  };
  
  const scrollToTop = () => {
    window.scrollTo({
      top: 0,
      behavior: 'smooth'
    });
  };
  
  onMounted(() => {
    window.addEventListener('scroll', handleScroll);
  });
  
  onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
  });
  </script>
  
  <style scoped>
  .back-to-top {
    position: fixed;
    bottom: 20px;
    right: 20px;
    padding: 12px 20px;
    background-color: var(--primary-color);
    color: white;
    border: solid 3px var(--secondary-color);
    border-radius: 50px;
    cursor: pointer;
    font-size: 22px;
    font-weight: 20;
    display: block;
    transition: opacity 0.3s ease;
    opacity: 0;
  }
  
  .back-to-top.show {
    display: block;
    opacity: 1;
  }
  
  .back-to-top:hover {
    background-color: var(--accent-color);
  }
  </style>
  