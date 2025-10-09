<template>
  <div id="contact" class="contact-card">
    <h1>Contact Me</h1>
    <p>Feel free to reach out!</p>

    <ul class="contact-list">
      <li>
        <i class="fa-solid fa-envelope"></i>
        <span>essi.antola@gmail.com</span>
        <i
          class="fa-regular fa-copy"
          :class="{ copied: copied }"
          @click="copyEmail"
          id="copy"
          style="color: #ffffff"
        ></i>
        <span v-if="copied" class="copied-text">Email copied!</span>
      </li>
      <li>
        <i class="fa-brands fa-linkedin"></i>
        <a
          href="https://fi.linkedin.com/in/essiantola"
          target="_blank"
          rel="noopener noreferrer"
          >LinkedIn</a
        >
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from "vue";

const copied = ref(false);

function copyEmail() {
  navigator.clipboard.writeText("essi.antola@gmail.com");
  copied.value = true;
  setTimeout(() => (copied.value = false), 1000);
}
</script>

<style scoped>
.contact-card {
  max-width: 600px;
  margin: 5rem auto;
  text-align: center;
  color: #fff;
}

.contact-card h1 {
  font-size: 3rem;
  margin-bottom: 0.5rem;
  letter-spacing: 1px;
}

.contact-card p {
  font-size: 1.1rem;
  margin-bottom: 2rem;
}

.contact-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  align-items: center;
}

.contact-list li {
  display: flex;
  align-items: center;
  gap: 0.8rem;
  font-size: 1.2rem;
}

.contact-list i {
  font-size: 1.5rem;
  color: #b78fff;
  transition: transform 0.3s, color 0.3s;
}

#copy:hover {
  transform: translateY(-3px);
}

a {
  color: #fff;
  text-decoration: none;
  transition: color 0.3s;
}

a:hover {
  color: #b78fff;
}

.copied-text {
  font-size: 1rem;
  color: #a082ff;
  transition: opacity 0.3s;
}
</style>
