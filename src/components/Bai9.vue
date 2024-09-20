<template>
  <div>
    <button @click="handleGender">Random gender</button>
    <h1>Random gender: {{ gender }}</h1>
  </div>
</template>

<script  setup>
import { ref } from 'vue';
const genders = ['Nam', 'Nữ', 'Khác'];
const gender = ref("Nam");
const handleGender=()=>{
    const randomIndex = Math.floor(Math.random() * genders.length);
    gender.value = genders[randomIndex];
}
</script>

<style>

</style>