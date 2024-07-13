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
    <div class="file-icon">
      <slot name="icon"></slot>
    </div>
    <div class="fsobj-name file-name">
      {{ filename }}
    </div>
  </div>
</template>

<!-- 


/* Inline #3 | http://localhost:5173/ */

.file-icon[data-v-98f2bf80] > * {
  /* height: 100%; */
  height: max(1rem);
}

/* Inline #3 | http://localhost:5173/ */

.file-item[data-v-98f2bf80] {
  height: 1rem;
  align-items: center;
  padding: 0.1rem;
  align-content: center;
  height: 1.8rem;
}

.file-name[data-v-98f2bf80] {
  height: 1rem;
  line-height: 1em;
}

.file-icon[data-v-98f2bf80] {
  /* height: 100%; */
  height: 1rem;
  margin: 0.05rem;
}

.file-icon[data-v-98f2bf80] > * {
  /* height: 1rem; */
  height: 100%;
}


-->
<style scoped>
.file-item {
  font-size: 16px;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0.1em;
  align-content: center;
  height: 1.8em;
}

.file-name {
  margin-left: 1em;
  height: 1em;
  line-height: 1em;
}
.file-icon {
  overflow: hidden;
  height: 100%;
  margin-top: 0.05em;
  margin-bottom: 0.05em;
}
.file-icon > :deep(*) {
  height: 1em;
}
</style>

