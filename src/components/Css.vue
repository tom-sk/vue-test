<script setup>
const css = defineModel()
</script>

<template>
  <div class="grid-cols-3 grid">
    <div class="col-span-1">
      <h4>CSS</h4>
    </div>

    <div class="col-span-2">
      <textarea v-model="css" class="w-full"/>
    </div>
  </div>
</template>
