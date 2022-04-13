<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import Hero from './components/Hero.vue';
import Showcase from './components/Showcase.vue';
import ArticlesShowcase from './components/ArticlesShowcase.vue';
</script>

<template>
  <Navbar></Navbar>
  <main class="main">
    <Hero></Hero>
    <Showcase></Showcase>
    <ArticlesShowcase></ArticlesShowcase>
  </main>
  <Footer></Footer>
</template>

<style lang="scss">
@import '@/sass/style.scss';

body {
  background-color: $neutral-900;
}

.main {
  max-width: 100%;
}
</style>
