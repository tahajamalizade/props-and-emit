<script setup>
defineProps(['msg'])
const emit = defineEmits(['msg'])

function changeMessage() {
  emit('msg', "پیام جدید از فرزند")
}
</script>

<template>
  <div style="margin-top:20px; border:1px solid gray; padding:10px">
    <h2>فرزند</h2>
    <p>پیام دریافتی از والد: {{ msg }}</p>
    <button @click="changeMessage">تغییر پیام</button>
  </div>
</template>
