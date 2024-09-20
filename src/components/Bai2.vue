<template>
  <div>
    <button @click="handleClick" v-if="isShow">ẩn</button>
    <button @click="handleClick" v-else="isShow">hiện</button>

  </div>
</template>

<script  setup>
import { ref } from 'vue';

const isShow = ref(true)



const handleClick=()=>{
    isShow.value=!isShow.value
}
</script>

<style>

</style>