<script setup>
defineProps(['msg'])
const emit = defineEmits(['msg'])

function changeMessage() {
  emit('msg', 'massi')
}
</script>

<template>
  <div style="margin-top: 20px; border: 1px solid gray; padding: 10px">
    <h2>childcomponent</h2>
    <p>{{ msg }}</p>
    <button @click="changeMessage"> changeMessage</button>
  </div>
</template>
