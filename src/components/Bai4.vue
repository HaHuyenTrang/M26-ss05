<template>
  <div>
    <button @click="handleClickShow">hiện</button>
    <button @click="handleClick">ẩn</button>
    <p>thông báo: <b v-if="isVisible"> Welcome to Rikkei Education</b></p>
  </div>
</template>

<script  setup>
import { ref } from 'vue';

const isVisible =ref(true)
const handleClickShow=()=>{
    isVisible.value=true
}
const handleClick=()=>{
    isVisible.value=false
}
</script>

<style>

</style>