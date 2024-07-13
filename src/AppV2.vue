<template>
  <div class="rt">
    <div class="file-item">
      <div class="file-icon-container">
        <img src="./assets/logo.svg" />
      </div>
      <div class="fsobj-name file-name">
        filename.vue
      </div>
    </div>
  </div>
</template>

<style>
.file-icon-container {
  display: grid;
  place-content: center;
}
.file-icon-container > * {
  width: 1.1em;
  height: 1.1em;
}
.file-icon-container > img {
  object-fit: contain;
}

.file-item {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0.1em;
  height: 1.8em;
}

.file-name {
  margin-left: 0.5em;
  height: 1em;
  line-height: 1em;
}
</style>
