<script setup>
import { ref } from 'vue'
import ChildComponent from './pages/ChildComponent.vue'

const message = ref('frst mass')

const secMessage = (newmass) => {
  message.value = newmass
}

const showDialog = ref(false)
</script>

<template>
  <div style="padding: 20px">
    <h4>parent</h4>
    <p>{{ message }}</p>

    <q-btn color="primary" label="باز کردن پاپ‌آپ" @click="showDialog = true" />

    <q-dialog v-model="showDialog">
      <q-card style="min-width: 400px; padding: 20px">
        <ChildComponent :msg="message" @msg="secMessage" />
        <div class="row justify-end q-gutter-sm">
          <q-btn flat label="clse" color="negative" v-close-popup />
        </div>
      </q-card>
    </q-dialog>
  </div>
</template>
