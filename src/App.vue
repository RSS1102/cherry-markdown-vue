<script setup lang="ts">
import CherryMarkdown from 'cherry-markdown'
import { ref, shallowRef } from 'vue';
const cherry = shallowRef();
cherry.value = new CherryMarkdown({
  id: 'cherry-markdown',
  value: '# test CherryMarkdown',
})

const setValue = () => {
  cherry.value.setValue('# Hello CherryMarkdown')
}

</script>

<template>
  <div id="cherry-markdown" />
  <button @click="setValue">Set Value</button>
</template>
