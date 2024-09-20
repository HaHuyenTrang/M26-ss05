<template>
  <div>
    <!-- <h1 v-if="number%2===0" >các số chẵn từ mảng: {{ number }}</h1> -->
     <h1 v-for="(number, index) in filterNumber()" :key="index">
        <div>{{ number }}</div>
     </h1>
   
  </div>
</template>

<script  setup>
import { reactive } from 'vue';

const number = reactive([1,2,3,4,5,6,7,8,9,10])
const filterNumber =()=>{
    const filterNumber=number.filter((item)=>item%2==0)
    return filterNumber
}
// const number =[1,2,3,4,5,6,7,8,9,10]

</script>

<style>

</style> 