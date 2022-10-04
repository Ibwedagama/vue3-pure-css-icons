<script setup lang="ts">
import { RouterView } from "vue-router";
</script>

<template>
  <div class="container">
    <header class="layout__header">
      <h1 class="layout__title">Pure CSS Icons</h1>
    </header>
    <RouterView />
  </div>
</template>

<style scoped>
.container {
  max-width: 1280px;
  width: 100%;
  margin: 0 auto;
}

.layout__header {
  padding: 3rem 0;
}

.layout__title {
  font-size: 3rem;
  font-weight: 700;
  text-align: center;
  margin-bottom: 2rem;
  background-color: #f3ec78;
  background-image: linear-gradient(
    64.5deg,
    rgba(245, 116, 185, 1) 14.7%,
    rgba(89, 97, 223, 1) 88.7%
  );
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
