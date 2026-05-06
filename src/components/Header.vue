<template>
  <header>
    <nav class="container nav-bar">
      <div class="brand">Muhammad Ikhwan Bin Ameri</div>

      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#skills">Skills</a></li>
      </ul>

      <div class="nav-actions">
        <a class="resume-button" href="resume.pdf" download>Download Resume</a>
        <button class="theme-toggle" type="button" @click="$emit('toggle-theme')" :aria-label="theme === 'dark' ? 'Switch to light theme' : 'Switch to dark theme'">
          <span>{{ theme === 'dark' ? '☀️ Light' : '🌙 Dark' }}</span>
        </button>
      </div>
    </nav>
  </header>
</template>

<script setup>
const props = defineProps({
  theme: {
    type: String,
    default: 'light',
  },
})
</script>