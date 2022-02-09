<script setup lang="ts">
  function change(e: Event) {
    if (!e) {
      return
    }
    const file = (document.getElementById('file') as unknown as HTMLInputElement)?.files
    console.log(file?.[0])
  }
</script>

<template>
  <div class="container">
    <div class="container_preview"></div>
    <div class="container_handle">
      <input type="file" id="file" @change="(e) => change(e)" />
      <div class="dropbox"></div>
    </div>
  </div>
</template>

<style lang="scss">
  .container {
    width: 100%;
    height: 95vh;
    display: flex;
    justify-content: space-between;
    &_preview {
      width: 49%;
      height: 100%;
      border: 1px solid #ccc;
      border-radius: 12px;
    }
    &_handle {
      width: 49%;
      height: 100%;
      border: 1px solid #ccc;
      border-radius: 12px;
      .dropbox {
        width: 80%;
        height: 200px;
        border: 1px dotted #ccc;
      }
    }
  }
</style>
