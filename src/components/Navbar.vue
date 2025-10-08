<script setup></script>

<template>
  <nav class="navbar">
    <div class="logo">
      <a href="#home">Essi Antola </a>
    </div>
    <ul class="center-links">
      <li><a href="#about">About Me</a></li>
      <li><a href="#tech-stack">Tech Stack</a></li>
      <li><a href="#projects">Projects</a></li>
    </ul>
    <ul class="contact-link">
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</template>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5em 2em;
  background-color: rgba(16, 12, 20, 0.849);
  color: white;
  font-size: 20px;
  position: sticky;
  top: 0;
  z-index: 1000;
}
.center-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
  margin: 0;
  padding: 0;
}
.contact-link {
  list-style: none;
}

.contact-link a {
  padding: 0.5em 1em;
  color: white;
  border-radius: 8px;
  text-decoration: none;
  background-color: #8b54e4;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
}

.contact-link a:hover {
  background-color: #8132c2;
  transform: translateY(-2px);
}

.center-links a {
  text-decoration: none;
  color: white;
  transition: color 0.3s;
}

.center-links a:hover {
  color: #60189b;
}

.logo {
  font-family: "VT323", monospace;
  font-weight: 400;
  font-size: 40px;
}

.logo a:hover {
  color: #c096d3;
}

a {
  font-weight: 500;
  color: #fafafa;
  text-decoration: inherit;
}
</style>
