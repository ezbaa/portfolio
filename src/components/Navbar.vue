<template>
  <nav class="navbar">
    <div class="logo">
      <a href="#home">Essi Antola </a>
    </div>
    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About Me</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="#resume">Download resume</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem 2rem;
  background-color: rgb(16, 12, 20);
  color: white;
  font-size: 20px;
}
.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
  margin: 0;
  padding: 0;
}

.nav-links a {
  text-decoration: none;
  color: inherit;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: #646cff;
}

.logo {
  font-family: "VT323", monospace;
  font-weight: 400;
  font-style: normal;
  font-size: 40px;
}
</style>
