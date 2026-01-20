<template>
  <section id="projects" class="projects">
    <h2>Projects</h2>

    <div class="projects-grid">
      <ProjectCard
        v-for="project in projects"
        :key="project.id"
        :title="project.title"
        :description="project.description"
        :image="project.image"
        :techStack="project.techStack"
        :githubUrl="project.githubUrl"
      />
    </div>
  </section>
</template>

<script setup>
import ProjectCard from "./ProjectCard.vue";

const projects = [
  {
    title: "Portfolio Website",
    description: "My personal porftolio",
    image: "/portfolio.png",
    techStack: ["Vue.js"],
    githubUrl: "https://github.com/ezbaa/portfolio",
  },
  {
    title: "Dev news Slack bot",
    description:
      "A bot that posts daily developer news to a Slack channel using Dev.to API. The project uses Python, Slack webhooks, and GitHub Actions for scheduling",
    image: "/slack_bot.png",
    techStack: ["Python"],
    githubUrl: "https://github.com/ezbaa/slack-dev-news-bot",
  },
];
</script>

<style scoped>
.projects {
  font-size: 1rem;
  padding: 2rem;
  text-align: center;
}

.projects-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
  margin-top: 2rem;
}
</style>
