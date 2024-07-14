<script setup>
import FileList from './components/FileList.vue';
</script>

<template>
  <main>
    <FileList :files-list="['main.js', 'App.vue', 'index.html', 'other', 'a.txt', 'M.json']"></FileList>
  </main>
</template>

<style>
</style>
