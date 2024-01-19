<script setup>
import Html from "./Html.vue";
import {onMounted, ref, watch} from "vue";
import Css from "./Css.vue";
import less from "less";

const html = ref('')
const css = ref('.test{' +
    'color: yellow;' +
    '}')
const compiledCss = ref('');

watch(css, (newCss, oldCss) => {
  less.render(newCss)
      .then(function (output) {
            compiledCss.value = '<style>' + output.css + '</style>';

            iframeContent.value.srcdoc = compiledCss.value + html.value;
          },
          function (error) {

          });
})

watch(html, () => {
  iframeContent.value.srcdoc = compiledCss.value + html.value;
})

onMounted(() => {
  compiledCss.value = '<style>' + css.value + '</style>';
  html.value = '<div class="test">Hello World!</div>'
})

const iframeContent = ref();
</script>

<template>
  <h2 class="text-3xl font-bold mb-8">Task 2</h2>

  <div class="grid grid-cols-2 gap-4 min-h-[300px] h-full">

    <div class="space-y-4">
      <Html v-model="html"/>

      <Css v-model="css"/>
    </div>

    <div>
      <iframe ref="iframeContent" class="w-full h-full"></iframe>
    </div>
  </div>
</template>
