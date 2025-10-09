<script setup>
function downloadCV() {
  const link = document.createElement("a");
  link.href = "/CV_EssiAntola.pdf";
  link.download = "CV_EssiAntola.pdf";
  link.click();
}
</script>

<template>
  <div class="hero" id="home">
    <div class="hero-content">
      <h1>Hi, I'm Essi,</h1>
      <h2>A Fullstack Developer</h2>
      <div class="links">
        <button type="button" @click="downloadCV">
          <i class="fa-solid fa-download"></i> CV
        </button>
        <a
          href="https://fi.linkedin.com/in/essiantola"
          target="_blank"
          rel="noopener noreferrer"
        >
          <i
            class="fa-brands fa-linkedin-in fa-xl"
            id="icon"
            style="color: #ffffff"
          ></i>
        </a>
        <a
          href="https://github.com/ezbaa"
          target="_blank"
          rel="noopener noreferrer"
        >
          <i
            class="fa-brands fa-github fa-xl"
            id="icon"
            style="color: #ffffff"
          ></i>
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero {
  width: 100%;
  height: 90vh;
  background-image: url("src/assets/hero_background.png");
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 30px;
}

.links {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
}

button {
  font-size: 20px;
  padding: 13px 25px;
  background-color: #9b59b6;
  color: #fff;
  cursor: pointer;
  transition: all 0.3s ease;
}

button:hover {
  background-color: #8b54e4;
  transform: translateY(-7px) scale(1.05);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
}

#icon:hover {
  transform: translateY(-7px) scale(1.05);
}

@media (max-width: 1024px) {
  .hero {
    height: 70vh;
    font-size: 24px;
  }

  .hero-content h1 {
    font-size: 3rem;
  }

  .hero-content h2 {
    font-size: 3rem;
  }
}

@media (max-width: 768px) {
  .hero {
    height: auto;
    min-height: 50vh;
    padding: 2em 1em;
    font-size: 20px;
  }

  .hero-content {
    flex-direction: column;
    gap: 1rem;
    text-align: center;
  }

  .hero-content h1,
  .hero-content h2 {
    font-size: 2rem;
  }

  .links {
    flex-direction: column;
    gap: 12px;
  }

  button {
    width: 40%;
    padding: 10px;
    max-width: 200px;
  }
}
</style>
