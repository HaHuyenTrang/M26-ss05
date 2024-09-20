<template>
  <div>
    <button @click="sortAscendingArr">tăng dần</button>

    <button @click="sortDescendingArr">giảm dần</button>
    <div>{{ arr }}</div>
  </div>
</template>

<script  setup>
import { reactive } from 'vue';

const arr = reactive([11,4,5,7,2,9,22,10])
const sortAscendingArr=()=>{
    const sortAscending = arr.sort((a,b)=>a-b)
    return sortAscending
}
const sortDescendingArr=()=>{
    const sortDescending = arr.sort((a,b)=>b-a)
    return sortDescending
}
</script>

<style>

</style>