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
    description: "Personal portfolio website built as a modern frontend application and deployed as a containerized service. The project focuses on clean UI, maintainable code, and production-like deployment practices.",
    image: "/portfolio.png",
    techStack: ["Vue.js"],
    githubUrl: "https://github.com/ezbaa/portfolio",
  },
  {
    title: "GitOps",
    description: "This repository contains the GitOps configuration used to deploy and operate my portfolio website on a Kubernetes cluster.",
    image: "workflow.png",
    techStack: ["Docker", "Kubernetes", "FluxCD"],
    githubUrl: "https://github.com/ezbaa/GitOps",
  },
  {
    title: "Dev news Slack bot",
    description:
      "A bot that posts daily developer news to a Slack channel using Dev.to API. The project uses Python, Slack webhooks and GitHub Actions for scheduling.",
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
