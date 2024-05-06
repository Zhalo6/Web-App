<script setup>
import { ref } from 'vue'

const text = ref('')
const count = ref(0)
const awesome = ref(true)

function onInput(e) {
  text.value = e.target.value
}

function increment() {
  count.value++
}

function toggle() {
  awesome.value = !awesome.value
}
  
</script>

<template>
  <div>
    <button @click="toggle">Toggle</button>
  </div>
  
  <div v-show="awesome">

  <input :value="text" @input="onInput" placeholder="Type here">
  <p>{{ text }}</p>
  <button @click="increment">Count is: {{ count }}</button>

  </div>
</template>