<template>
  <div>
    <p v-if="role==='admin'"> quyền của bạn là {{ role }}</p>
    <p v-if="role==='user'"> quyền của bạn là {{ role }}</p>
    <p v-if="role==='gues'"> quyền của bạn là {{ role }}</p>
  </div>
</template>

<script  setup>
import { ref } from 'vue';

const role = ref("user");
</script>

<style>

</style>