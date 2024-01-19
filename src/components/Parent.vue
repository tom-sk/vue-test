<script setup>
import {ref} from "vue";
import Child from "./Child.vue";

const bool = ref(false);
const text = ref('The text');
</script>

<template>
<div class="grid grid-cols-1">
  <h1 class="text-4xl font-bold mb-8">Task #1</h1>
  <div class="mb-8 space-y-2">
    <h2 class="text-2xl font-bold">Parent</h2>

    <div>Bool: {{bool}}</div>

    <div>Text: {{text}}</div>
  </div>

  <Child v-model:bool="bool" v-model:text="text"/>
</div>
</template>

