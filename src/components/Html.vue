<script setup>
const html = defineModel()
</script>

<template>
<div class="grid-cols-3 grid">
  <div class="col-span-1">
    <h4>HTML</h4>
  </div>

  <div class="col-span-2">
    <textarea v-model="html" class="w-full"/>
  </div>
</div>
</template>
