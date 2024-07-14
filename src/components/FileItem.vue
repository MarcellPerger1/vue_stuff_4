<script setup>
import { computed } from 'vue';

const props = defineProps({
  filename: {
    type: String,
    required: true
  }
});

function getSuffix(/** @type {string} */fileName) {
  let dotParts = fileName.split('/').at(-1).split(".");
  return dotParts.length <= 1 ? '' : dotParts.at(-1);
}
function isLightMode() {
  if(matchMedia('(prefers-color-scheme: light)').matches) {
    return true;
  }
  return false;
}

/** @type {{[k: string]: string | {light: string, dark: string}}} */
var logosMap = {
  js: "js.svg", 
  vue: "vue.svg",
   '': {
    light: 'unknown-light.svg',
    dark: 'unknown-dark.svg'
  }
};

function getLogoNameFor(filename) {
  let result = logosMap[getSuffix(filename)];
  if(typeof result === 'string') return result;
  return isLightMode() ? result.light : result.dark;
}
function getLogoPathFor(filename) {
  return `/logos/${getLogoNameFor(filename)}`;
}
const logoSrc = computed(() => {
  return getLogoPathFor(props.filename);
});

</script>

<template>
  <div class="file-item">
    <div class="file-icon-container">
      <img :src="logoSrc" />
    </div>
    <div class="fsobj-name file-name">
      {{ filename }}
    </div>
  </div>
</template>

<style scoped>
.file-icon-container {
  display: grid;
  place-content: center;
}
.file-icon-container > :deep(*) {
  width: 1.0em;
  height: 1.0em;
}
.file-icon-container > :deep(img) {
  object-fit: contain;
}

.file-item {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0.1em;
  padding-left: 0.4em;
  height: 1.8em;
}

.fsobj-name {
  margin-left: 0.5em;
  height: 1em;
  line-height: 1em;
}
</style>
