<script setup lang="ts">
import { watch } from "vue";
import useCounterStore from "../stores/counterStore";

const counterStore = useCounterStore();

watch([counterStore], () => console.log("wowww"));

const reset = () => {
  counterStore.$reset();
};
</script>

<template>
  <div>
    <h1>Counter View: {{ counterStore.counter }}</h1>
    <button @click="counterStore.incrementBy(1)">+1</button>
    <button @click="counterStore.incrementBy(2)">+2</button>
    <button @click="counterStore.incrementBy(3)">+3</button>
    <button @click="reset">Reset</button>
  </div>
</template>
