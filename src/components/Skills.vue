<template>
  <section class="tech-stack" id="tech-stack">
    <h2>Tech Stack</h2>

    <div class="category">
      <h3>Frontend</h3>
      <div class="skills">
        <div class="skill-card">
          <i class="fa-brands fa-js fa-2xl" style="color: #f7df1e"></i>
          <span>JavaScript</span>
        </div>
        <div class="skill-card">
          <i class="fa-brands fa-vuejs fa-2xl" style="color: #42b883"></i>
          <span>Vue.js</span>
        </div>
        <div class="skill-card">
          <i class="fa-brands fa-css fa-2xl" style="color: #1572b6"></i>
          <span>CSS</span>
        </div>
        <div class="skill-card">
          <i class="fa-brands fa-html5 fa-2xl" style="color: #e34f26"></i>
          <span>HTML</span>
        </div>
      </div>
    </div>

    <div class="category">
      <h3>Backend</h3>
      <div class="skills">
        <div class="skill-card">
          <i class="fa-brands fa-python fa-2xl" style="color: #306998"></i>
          <span>Python</span>
        </div>
        <div class="skill-card">
          <i class="fa-solid fa-database fa-2xl" style="color: #4db8ff"></i>
          <span>Django</span>
        </div>
        <div class="skill-card">
          <i class="fa-solid fa-bolt fa-2xl" style="color: #2596be"></i>
          <span>FastAPI</span>
        </div>
        <div class="skill-card">
          <i class="fa-solid fa-server fa-2xl" style="color: #4945fe"></i>
          <span>Strapi</span>
        </div>
      </div>
    </div>

    <div class="category">
      <h3>DevOps</h3>
      <div class="skills">
        <div class="skill-card">
          <i class="fa-brands fa-docker fa-2xl" style="color: #0db7ed"></i>
          <span>Docker</span>
        </div>
        <div class="skill-card">
          <i class="fa-solid fa-cubes fa-2xl" style="color: #326ce5"></i>
          <span>Kubernetes</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
i {
  margin-top: 1rem;
}

h3 {
  font-family: "Lato", sans-serif;
  font-weight: 400;
  font-style: normal;
  line-height: 1.6;
  font-size: 1.2em;
  font-weight: bold;
}

.tech-stack {
  padding: 2rem;
  text-align: center;
}

.category {
  margin-bottom: 2rem;
}

.skills {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1.5rem;
  margin-top: 2rem;
}

.skill-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1.6rem;
  border-radius: 12px;
  background-color: rgba(255, 255, 255, 0.05);
  width: 100px;
  transition: transform 0.3s, background-color 0.3s;
}

.skill-card:hover {
  transform: translateY(-5px);
  background-color: rgba(255, 255, 255, 0.1);
}

.skill-card span {
  margin-top: 1.2rem;
  font-size: 1.2rem;
  color: #fafafa;
}
</style>
