<template>
  <div>
    <h1 v-if="isShow">Rikkei Academy</h1>
    <button @click="handleClick">show</button>
  </div>
</template>

<script  setup>
import { ref } from 'vue';

const isShow= ref(true)
const handleClick=()=>{
    isShow.value=!isShow.value
}
</script>

<style>

</style>