<template>
  <div class="project-card">
    <img v-if="image" :src="image" alt="" class="project-image" />

    <h3>{{ title }}</h3>

    <a
      class="github-button"
      :href="githubUrl"
      target="_blank"
      rel="noopener noreferrer"
    >
      <i class="fa-brands fa-github fa-xl" id="icon" style="color: #ffffff"></i>
      View code
    </a>

    <p class="description">
      {{ description }}
    </p>

    <div class="tech">
      <span v-for="tech in techStack" :key="tech" class="tech-item">
        {{ tech }}
      </span>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  image: String,
  techStack: Array,
  githubUrl: String,
});
</script>

<style scoped>
.project-card {
  background-color: rgba(255, 255, 255, 0.05);
  border-radius: 16px;
  padding: 1.8rem;
  width: 320px;
  text-align: center;
  transition:
    transform 0.3s,
    background-color 0.3s;
  border: 1px solid rgba(148, 163, 184, 0.25);
  position: relative;
}

.project-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 4px;
  width: 100%;
  background: linear-gradient(90deg, #2dd4bf, #8b5cf6);
  border-radius: 16px 16px 0 0;
}

.project-card:hover {
  transform: translateY(-6px);
  background-color: rgba(255, 255, 255, 0.1);
}

.project-image {
  width: 100%;
  border-radius: 12px;
  margin-bottom: 1rem;
}

.tech {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 0.6rem;
  margin-bottom: 1.4rem;
}

.tech-item {
  background-color: rgba(255, 255, 255, 0.1);
  padding: 0.3rem 0.8rem;
  border-radius: 999px;
  font-size: 0.9rem;
}

.github-button {
  display: inline-block;
  padding: 0.6rem 1.2rem;
  margin-bottom: 1rem;
  border-radius: 8px;
  background-color: #24292e;
  color: #fff;
  text-decoration: none;
  font-size: 0.95rem;
}

.github-button:hover {
  background-color: #333;
}

h3 {
  font-size: 50px;
  margin-top: 1rem;
  margin-bottom: 2rem;
}
</style>
