<script setup lang="ts">
import "./assets/style.css"
import './assets/variables.css';

import HeaderBar from './components/NavBar.vue';
import Home from "./components/Home.vue";
import Projects from "./components/Projects.vue"
import Contact from "./components/Contact.vue"
</script>

<template>
  <header>
    <HeaderBar />

  </header>

  <main>
    <Home />
    <Projects />
    <Contact />
  </main>
</template>

<style scoped>
</style>
