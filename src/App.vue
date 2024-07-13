<script setup>
import FileList from './components/FileList.vue';
</script>

<template>
  <main>
    <FileList :files-list="['main.js', 'App.vue', 'other']"></FileList>
  </main>
</template>

<style>
</style>
