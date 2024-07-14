<script setup>
import FileList from './components/FileList.vue';
import AddFileButton from './components/AddFileButton.vue';
import { ref } from 'vue';

const /** @type {import('./components/FileList.vue').default} */ fileList = ref(null);

</script>

<template>
  <main>
    <FileList :inital-files="['main.js', 'App.vue', 'index.html', 'other', 'a.txt', 'M.json']" ref="fileList"></FileList>
    <AddFileButton @add-file="fileList.addItem('abc.vue.js')" />
  </main>
</template>

<style>
</style>
