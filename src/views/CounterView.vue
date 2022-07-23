<script setup lang="ts">
import useCounterStore from "../stores/counterStore";

const counterStore = useCounterStore();
</script>

<template>
  <div>
    <h1>Counter View: {{ counterStore.counter }}</h1>
    <button @click="counterStore.incrementBy(1)">+1</button>
    <button @click="counterStore.incrementBy(2)">+2</button>
    <button @click="counterStore.incrementBy(3)">+3</button>
  </div>
</template>
