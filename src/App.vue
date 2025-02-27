<script setup>
import CounterButton from "./components/CounterButton.vue"
import CounterReset from "./components/CounterReset.vue";
import { useCounter } from "./stores/counter";
const counter = useCounter()


counter.$subscribe((mutation,state)=>{
  console.log(mutation,state)
})
</script>

<template>
  <h1>Curs 1</h1>
  <h2>Counter from Store is: {{ counter.count }}</h2>
  <h2>Level from Store is: {{ counter.level }}</h2>

  <CounterButton />  
  <hr />
  <CounterReset />

</template>
