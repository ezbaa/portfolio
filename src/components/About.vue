<script setup></script>

<template>
  <div id="about" class="card">
    <h1>About me</h1>

    <p>
      Hey there! I'm Essi, a developer from Finland. I recently graduated as a
      software developer and completed a six-month internship where I worked on
      both frontend and backend projects. I enjoy full-stack development,
      taking features from concept to deployment and understanding how code
      flows from the user interface to the server and into production.
      Right now, I’m focused on growing as a full-stack developer, exploring new tools,
      and building projects that challenge me.
    </p>
  </div>
</template>

<style scoped>
.card {
  font-size: 20px;
  max-width: 80ch;
  margin: 0 auto;
  text-align: left;
  letter-spacing: 0.5px;
}

@media (max-width: 1024px) {
  .card {
    font-size: 18px;
    padding: 0 2em;
  }
}

@media (max-width: 768px) {
  .card {
    font-size: 0.8em;
    text-align: center;
    padding: 0 1.5em;
  }
}
</style>
