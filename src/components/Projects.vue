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
        :action="project.action"
      />
    </div>
  </section>
</template>

<script setup>
import ProjectCard from "./ProjectCard.vue";

const projects = [
    {
    title: "Food Macro API",
    description: "A food analysis API that uses a vision LLM to identify dishes and estimate macronutrients from photos. Secured with GitHub OAuth2 authentication and deployed on Kubernetes.",
    image: "food_macro_api.png",
    techStack: ["Python", "FastAPI", "Vue.js", "Groq API"],
    githubUrl: "https://github.com/ezbaa/food-macro-api",
    action: [
      { text: "Watch demo", url: "https://www.loom.com/share/329621413ba949b0b04df3e395bacd6c", icon: ["fa-solid", "fa-video"]},
      { text: "Live site (whitelisted access)", url: "https://essiantola.com/food-macro/", icon: ["fa-solid", "fa-arrow-up-right-from-square"]}
    ]
  },
  {
    title: "Portfolio Website",
    description: "Personal portfolio website built with Vue.js, containerized with Docker and deployed on a Kubernetes cluster via GitOps workflow.",
    image: "/portfolio.png",
    techStack: ["Vue.js", "Docker", "Kubernetes"],
    githubUrl: "https://github.com/ezbaa/portfolio",
  },
  {
    title: "GitOps",
    description: "GitOps configuration for deploying and managing my portfolio on a self-hosted Kubernetes cluster using FluxCD for automated, Git-driven deployments",
    image: "workflow.png",
    techStack: ["Docker", "Kubernetes", "FluxCD"],
    githubUrl: "https://github.com/ezbaa/GitOps",
  },
  {
    title: "Dev news Slack bot",
    description:
      "A bot that posts daily developer news to a Slack channel using Dev.to API. For each article, it provides an AI-generated summary.",
    image: "slack_bot.png",
    techStack: ["Python", "Groq API", "Dev.to API", "Slack API", "GitHub Actions"], 
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
