<script setup>
const text = defineModel('text')
const bool = defineModel('bool')
</script>

<template>
  <div class="bg-blue-400 p-4 grid grid-cols-1 space-y-2 rounded">
    <h2 class="text-2xl font-bold">Child</h2>

    <div>Bool: {{bool}}</div>

    <div>Text: {{text}}</div>

    <div class="grid grid-cols-2 gap-4">
      <input type="text" v-model="text">

      <label class="cursor-pointer">
        <input type="checkbox" v-model="bool">
        Toggle the bool
      </label>
    </div>


  </div>
</template>
