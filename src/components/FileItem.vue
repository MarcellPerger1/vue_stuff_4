<script setup>
defineProps({
  filename: {
    type: String,
    required: true
  }
});
</script>

<template>
  <div class="rt">
    <div class="file-item">
      <div class="file-icon-container">
        <img src="../assets/logo.svg" />
      </div>
      <div class="fsobj-name file-name">
        {{ filename }}
      </div>
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
  height: 1.8em;
}

.fsobj-name {
  margin-left: 0.5em;
  height: 1em;
  line-height: 1em;
}
</style>
