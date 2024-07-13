<script setup>
import FileItem from './FileItem.vue';
defineProps({
  filesList: {
    required: true,
    type: Array
  }
});
</script>

<template>
  <FileItem v-for="fname in filesList" :key="fname" :filename="fname" />
</template>
