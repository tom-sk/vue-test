<script setup>
import Parent from "./components/Parent.vue";
import Compiler from "./components/Compiler.vue";
</script>

<template>
  <div class="bg-red-300 p-4 mx-auto max-w-5xl m-8 rounded shadow">
    <Parent/>
  </div>

  <div class="mx-auto max-w-5xl m-8 bg-gray-400 rounded shadow p-4">
    <Compiler/>
  </div>
</template>
