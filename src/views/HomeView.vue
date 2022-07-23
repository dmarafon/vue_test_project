<script setup lang="ts">
import useCounterStore from "../stores/counterStore";

const counterStore = useCounterStore();
</script>

<template>
  <div>
    <h1>Home View: {{ counterStore.counter }}</h1>
    <h2>Number of Changes {{ counterStore.numberOfChanges }}</h2>
  </div>
</template>
