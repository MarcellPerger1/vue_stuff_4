<script setup>
defineProps({
  filename: {
    type: String,
    required: true
  }
});
</script>

<template>
  <div class="file-item">
      <div class="ico-container">
        <img class="ic" src="./assets/logo.svg" />
      </div>
      <div class="fsobj-name file-name">
        {{ filename }}
      </div>
    </div>
</template>

<style scoped>
.ico-container {
  display: grid;
  place-content: center;
}

.file-item {
  font-size: 16px;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0.1em;
  height: 1.8em;
}

.file-name {
  margin-left: 1em;
  height: 1em;
  line-height: 1em;
}

.ic {
  width: 1.1em;
  max-height: 1.4em;
}
</style>

