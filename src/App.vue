<script setup>
import { ref, onMounted } from 'vue'
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
import Footer from './components/Footer.vue'

const theme = ref('light')

const setTheme = (value) => {
  theme.value = value
  document.documentElement.dataset.theme = value
  localStorage.setItem('theme', value)
}

const toggleTheme = () => {
  setTheme(theme.value === 'light' ? 'dark' : 'light')
}

onMounted(() => {
  const storedTheme = localStorage.getItem('theme')
  const preferred = window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light'
  setTheme(storedTheme || preferred)
})
</script>

<template>
  <div>
    <Header :theme="theme" @toggle-theme="toggleTheme" />
    <Hero />
    <Projects />
    <Skills />
    <Contact />
    <Footer />
  </div>
</template>
