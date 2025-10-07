<script setup></script>
<template>
  <div>
    <h1>Contact me!</h1>
    <form id="contact">
      <input type="text"></input>
      <input type="text"></input>
      <input type="text"></input>

    </form>

  </div>
</template>

<style scoped>
form{
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 1em;

}

input, textarea {
  width: 100%;
  max-width: 500px;
}
</style>
