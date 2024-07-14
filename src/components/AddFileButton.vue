<script setup>
defineEmits(['add-file']);
</script>

<template>
  <div class="add-file-button">
    <button @click.left="$emit('add-file')">+ Add File</button>
  </div>
</template>

<style scoped>
.add-file-button {
  padding-left: 0.4em;
}
</style>