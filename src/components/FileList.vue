<script setup>
import FileItem from './FileItem.vue';
defineProps({
  filesList: {
    required: true,
    type: Array
  }
});

function sortedIgnoreCase(/** @type {string[]} */ls) {
  return ls.slice().sort((a, b) => {
    a = a.toLowerCase();
    b = b.toLowerCase();
    return (
      a == b ? 0 
      : a < b ? -1 
      : 1
    );
  });
}

</script>

<template>
  <FileItem v-for="fname in sortedIgnoreCase(filesList)" :key="fname" :filename="fname" />
</template>
