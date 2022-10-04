<script setup lang="ts">
import { ref } from "vue";

import SVGIcon from "../components/SVGIcon.vue";

const colorPicker = ref("#5961df");
const sizeInput = ref(24);
</script>

<template>
  <main class="home">
    <section class="home__section">
      <h2 class="home__title">
        Use SVG Icon as Vue Component
        <code class="code-block">
          &lt;SVGIcon icon="instagram.svg" fill-color="#000" :size="24"&gt;
        </code>
      </h2>
      <div class="home__icons">
        <div class="icons__container">
          <SVGIcon icon="instagram.svg" :size="24" />
        </div>
        <div class="icons__container">
          <SVGIcon icon="bell.svg" :size="24" />
        </div>
        <div class="icons__container">
          <SVGIcon icon="book.svg" :size="24" />
        </div>
        <div class="icons__container">
          <SVGIcon icon="thumbs-up.svg" :size="24" />
        </div>
      </div>
    </section>

    <section class="home__section">
      <h2 class="home__title">Change Color and Size Dynamically</h2>
      <div class="toolbar">
        <div class="input-group">
          <label class="input-group__label" for="color-picker">
            Pick a Color
          </label>
          <input
            class="input-group__input"
            type="color"
            id="color-picker"
            name="color-picker"
            v-model="colorPicker"
          />
        </div>
        <div class="input-group">
          <label class="input-group__label" for="size"> Change size </label>
          <input
            class="input-group__input"
            type="number"
            id="size"
            name="size"
            v-model="sizeInput"
          />
        </div>
      </div>

      <div class="home__icons">
        <div class="icons__container">
          <SVGIcon
            icon="instagram.svg"
            :size="sizeInput"
            :fill-color="colorPicker"
          />
        </div>
        <div class="icons__container">
          <SVGIcon
            icon="bell.svg"
            :size="sizeInput"
            :fill-color="colorPicker"
          />
        </div>
        <div class="icons__container">
          <SVGIcon
            icon="book.svg"
            :size="sizeInput"
            :fill-color="colorPicker"
          />
        </div>
        <div class="icons__container">
          <SVGIcon
            icon="thumbs-up.svg"
            :size="sizeInput"
            :fill-color="colorPicker"
          />
        </div>
      </div>
    </section>

    <section class="home__section">
      <h2 class="home__title">Works with Monochrome and Colored Icons</h2>
      <div class="home__icons">
        <div class="icons__container">
          <SVGIcon icon="cherry.svg" :size="32" mode="image" />
        </div>
        <div class="icons__container">
          <SVGIcon icon="star.svg" :size="32" />
        </div>
        <div class="icons__container">
          <SVGIcon icon="banana.svg" :size="32" mode="image" />
        </div>
        <div class="icons__container">
          <SVGIcon icon="smile.svg" :size="32" />
        </div>
      </div>
    </section>

    <section class="home__section">
      <h2 class="home__title">
        Just put your SVG Icons on
        <code class="code-block">src/assets/icons</code>
        <span>as simple as that ❤️</span>
      </h2>
    </section>
  </main>
</template>

<style scoped>
.home__title {
  font-size: 1.5rem;
  line-height: 150%;
  margin-bottom: 2rem;
  font-weight: 500;
  text-align: center;
}

.home__section {
  background: #eee;
  padding: 3rem 2rem;
  margin: 0 2rem;
  border-radius: 12px;
  border: 1px solid #eee;
  margin-bottom: 6rem;
  box-shadow: rgba(245, 116, 185, 0.5) 0px 7px 29px 0px;
}

.home__icons {
  min-width: 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 2rem;
}

.icons__container {
  min-width: 90px;
  min-height: 90px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 12px;
  border: 1px solid rgb(219, 219, 219);
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}

.toolbar {
  display: flex;
  flex-wrap: wrap;
  column-gap: 4rem;
  row-gap: 2rem;
  justify-content: center;
  align-items: center;
  margin-bottom: 2rem;
}

.input-group {
  display: flex;
  flex-direction: column;
}

.input-group__input {
  height: 2rem;
  border: 1px solid rgb(219, 219, 219);
}

.input-group__input[type="number"] {
  padding: 0 0.5rem;
}

.input-group__label {
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
}

.code-block {
  display: block;
  width: fit-content;
  margin: 0 auto;
  margin-top: 1rem;
  font-weight: 500;
  background: #282a36;
  color: #ff79c6;
  padding: 0.5rem 1rem;
  border-radius: 4px;
  font-size: 0.875rem;
  font-family: "Fira Code", monospace;
}
</style>
