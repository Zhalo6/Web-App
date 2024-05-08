<script setup>
import { ref } from 'vue'

const text = ref('')
const count = ref(0)
const awesome = ref(true)

function onInput(e) {
  text.value = e.target.value
}

function toggle() {
  awesome.value = !awesome.value
}
  
</script>

<style>
  .background {
    position: absolute;
    top: 0%;
    left: 0%;
    width: 1920px;
    height: 1080px;
    background: #102531;
  }
  .center {
    position: absolute;
    top: 150%;
    left: 50%;
    transform: translate(-50%, -50%);
    padding: 10px;
    background: #09202D;
    box-shadow: 0px 4px 8px 3px rgba(0, 0, 0, 0.15), 0px 1px 3px rgba(0, 0, 0, 0.3);
    border-radius: 4px;
  }
  .buttonOne {
    position: absolute;
    top: 250%;
    left: 25%;
    transform: translate(-50%, -50%);
    padding: 10px;
    background: #09202D;
    box-shadow: 0px 7px 21px rgba(0, 0, 0, 0.2);
    border-radius: 6px;
  }
  .buttonTwo {
    position: absolute;
    top: 250%;
    left: 50%;
    transform: translate(-50%, -50%);
    padding: 10px;
    background: #09202D;
    box-shadow: 0px 7px 21px rgba(0, 0, 0, 0.2);
    border-radius: 6px;
  }
  .buttonThree {
    position: absolute;
    top: 250%;
    left: 75%;
    transform: translate(-50%, -50%);
    padding: 10px;
    background: #09202D;
    box-shadow: 0px 7px 21px rgba(0, 0, 0, 0.2);
    border-radius: 6px;
  }
</style>

<template>
  <div class="background"></div>
  <div class="center">
    <input :value="text" @input="onInput" placeholder="Enter Champion...">
  </div>
  <div class="buttonOne">
    <button>Team Comps</button>
  </div>
  <div class="buttonTwo">
    <button>Best In Slot</button>
  </div>
  <div class="buttonThree">
    <button>Augments</button>
  </div>
</template>