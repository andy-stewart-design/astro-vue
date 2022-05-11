<script setup lang="ts">
import { ref } from "vue";
const test: string = "This is a headline";

let isActive = ref<boolean>(false);
function toggleActive() {
  isActive.value = !isActive.value;
}
</script>

<template>
  <section class="px-8 py-24 min-h-screen">
    <h1>{{ test }} {{ isActive }}</h1>
    <button
      class="btn px-4 py-2 text-white bg-black rounded-full"
      @click="toggleActive"
      :class="{ active: !isActive }"
    >
      Click Me
    </button>
  </section>
</template>

<style>
.btn {
  background: black;
}
.btn.active {
  background: blue;
}
</style>
