<!-- JS -->
<script setup>
import { ref } from "vue";

const msg = ref("hello");
const ok = ref(true);
const eventName = ref("click")

function change() {
  msg.value = msg.value === 'changed' ? "hello" : "changed";
  // ok.value = !ok.value
}


</script>

<!-- Template -->
<template>
  <h1>{{ msg }}</h1>
  <h1>{{ ok ? "true" : "false"}} </h1>
  <button @[eventName]="ok=!ok" @dblclick="change">Click</button>

  <h1 v-if="ok">Hello this tag has shown now </h1>
</template>

<!-- Style -->
<style scoped></style>
