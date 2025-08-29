<script setup>
import { ref } from 'vue'
import ChildComponent from './pages/ChildComponent.vue'

const message = ref('پیام اولیه از والد')
</script>

<template>
  <div style="padding: 20px">
    <h1>والد</h1>
    <p>پیام فعلی: {{ message }}</p>

    <ChildComponent :msg="message" @msg="message = $event" />
  </div>
</template>
