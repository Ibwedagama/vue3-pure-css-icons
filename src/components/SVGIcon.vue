<template>
  <span
    v-bind:style="computedStyle"
    aria-label="SVG Icon"
    aria-roledescription="SVG Icon"
  />
</template>

<script lang="ts">
export default {
  name: "SVGIcon",
};
</script>

<script setup lang="ts">
import { computed } from "vue";

const props = defineProps({
  /**
   * Name of the icon file
   * relative to ./src/assets/icons folder
   */
  icon: {
    type: String,
    default: "",
  },
  /**
   * Size of icon in pixel
   */
  size: {
    type: Number,
    default: 16,
  },
  /**
   * Fill color of the icon
   */
  fillColor: {
    type: String,
    default: "#000",
  },
  /**
   * Use mode = "mask" for monochrome icons
   * and use mode = "image" for colored icons
   */
  mode: {
    type: String,
    default: "mask",
    validator(value: string) {
      // The value must match one of these strings
      return ["mask", "image"].includes(value);
    },
  },
});

const getImageUrl = (name: string) => {
  const imageUrl = new URL(`../assets/icons/${name}`, import.meta.url).href;
  return imageUrl;
};

const computedStyle = computed(() => {
  if (props.mode === "mask") {
    return {
      display: "block",
      "background-color": props.fillColor,
      "mask-image": `url(${getImageUrl(props.icon)})`,
      "mask-size": "100% 100%",
      height: `${props.size}px`,
      width: `${props.size}px`,
    };
  } else {
    return {
      background: `url(${getImageUrl(props.icon)}) no-repeat`,
      "background-size": "100% 100%",
      "background-color": "transparent",
      height: `${props.size}px`,
      width: `${props.size}px`,
    };
  }
});
</script>
