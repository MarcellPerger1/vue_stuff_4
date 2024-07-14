<script setup>
import { reactive } from 'vue';
import FileItem from './FileItem.vue';

const props = defineProps({
  initalFiles: {
    type: Array,
    default: () => [],
  }
});

const files = reactive(props.initalFiles);

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

function addItem(item) {
  if(files.includes(item)) {
    throw new Error("Item is already present");
  }
  files.push(item);
}

defineExpose({
  addItem
});
</script>

<template>
  <FileItem v-for="fname in sortedIgnoreCase(files)" :key="fname" :filename="fname" />
</template>
