<script setup lang="ts">
import { RouterView } from "vue-router";
</script>

<template>
  <div class="container">
    <header class="layout__header">
      <h1 class="layout__title">Pure CSS Icons</h1>
      <h2 class="layout__subtitle">
        This approach is inspired by
        <a
          href="https://antfu.me/posts/icons-in-pure-css"
          target="_blank"
          rel="noopener"
          class="links"
        >
          Anthony Fu's Blog Post: Pure CSS Icons
        </a>
      </h2>
    </header>
    <RouterView />
    <footer class="layout__footer">
      <h2 class="layout__subtitle">
        Clone the repo
        <br />
        <a
          href="https://github.com/Ibwedagama/vue3-pure-css-icons"
          rel="noopener"
          class="links"
          title="Github Repo"
        >
          Ibwedagama/vue3-pure-css-icons
        </a>
      </h2>
    </footer>
  </div>
</template>

<style scoped>
.container {
  box-sizing: border-box;
  max-width: 1280px;
  width: 100%;
  margin: 0 auto;
  padding: 0 1rem;
}

.layout__header,
.layout__footer {
  padding: 3rem 0;
}

.layout__title {
  font-size: 3rem;
  line-height: 120%;
  font-weight: 700;
  text-align: center;
  margin-bottom: 2rem;
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

.layout__subtitle {
  font-size: 1.2rem;
  line-height: 180%;
  text-align: center;
  color: white;
  margin-bottom: 2rem;
}

.links {
  font-size: 1.2rem;
  font-weight: 500;
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
  text-decoration: underline;
  text-decoration-color: linear-gradient(
    64.5deg,
    rgba(245, 116, 185, 1) 14.7%,
    rgba(89, 97, 223, 1) 88.7%
  );
  text-align: center;
}
</style>
