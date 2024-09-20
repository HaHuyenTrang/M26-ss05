<template>
    <div>
      <h1>Countcomponents</h1>
      <h2>Count: {{ count }}</h2>
      <button @click="handleCount">Count</button>
      <button @click="handleRandom">random</button>
      <h2>Random: {{ random }}</h2>
      <button @click="handleNumber">Push number</button>
      <h2>{{ pushNumber }}</h2>
    </div>
  </template>
  
  <script  setup>
  import { ref } from 'vue';
  // khi dùng ref để cập nhật lại giá trị thì phải truy cập vào value
  let count = ref(0);
  const handleCount =()=>{
  // cập nhật giá trị count
  count.value++;
  }
  
  let random = ref(0)
  const handleRandom =()=>{
      random.value=Math.ceil(Math.random()*10)
  }
  
  let pushNumber =ref ([])
  const handleNumber =()=>{
    const  random=Math.ceil(Math.random()*10)
    pushNumber.value.push(random)
  }
  </script>
  
  <style>
  
  </style>