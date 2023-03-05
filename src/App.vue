<script setup>
import Main from "./components/Main.vue";
</script>

<template>
  <div class="container">
    <Main />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  max-height: 100vh;
  overflow: hidden;
}
</style>
