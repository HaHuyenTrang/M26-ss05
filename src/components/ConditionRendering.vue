<template>
  <div>
    <h1 v-if="isShow">Condition Rendering component</h1>
    <button @click="handleClick">Toggle</button>
    <h1 v-if="age >=18">{{age}}: đủ tuổi thi</h1>
    <h1 v-else="age">{{age}}: chưa đủ tuổi</h1>
    <button @click="handleup">tăng tuổi</button>
    <button @click="handledown">giảm tuổi</button>
    <h3 v-if="role==='admin'">đây là quyền {{ role }}</h3>
    <h3 v-if="role==='user'">đây là quyền {{ role }}</h3>
    <h3 v-if="role==='edit'">đây là quyền {{ role }}</h3>
    <h3 v-else>đây là quyền other</h3>
    <!-- v-show: hiển thị dữ liệu có điều kiện, tuy nhiên là dữ liệu kh bị xóa khỏi DOM -->
     <h1 v-show="isShowForm">Form content</h1>


  </div>
</template>

<script  setup>

import { ref } from 'vue';
const isShowForm = ref(true)
const isShow = ref(true);
const handleClick =()=>{
    isShow.value=!isShow.value
}
// tạo 1 biến, nếu tuổi trên 18 thì hiển thị đủ tuổi thi, ngược lại chưa đủ tuổi thi
const age = ref(0)
const handleup=()=>{
   age.value++;
}
const handledown=()=>{
   age.value--;
}

// ktra đk render quyền
const role = ref("")

</script>

<style>

</style>