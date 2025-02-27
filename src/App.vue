<script setup>
import Counter from "./components/counter.vue"

import { useCounter } from "./stores/counter";
const counter = useCounter()
</script>

<template>
  <h1>Curs 1</h1>
  <h2>Counter from Store is: {{ counter.count }}</h2>

  <Counter />  
  <br />
  <Counter />
</template>
