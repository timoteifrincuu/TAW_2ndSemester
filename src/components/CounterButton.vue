<script setup>
import { useCounter } from '../stores/counter'

const counter = useCounter()

function countUp() {
  counter.count++
  if (counter.count % 5==0){
      counter.level++
  }

  counter.$patch(
    {
      count: counter.count++,
      level: counter.level++
    }
  )
}
</script>

<template>
 <button @click="countUp">count is {{ counter.count }}</button>
</template>