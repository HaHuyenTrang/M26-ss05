<template>
  <div>
    <h1>List Rendering</h1>
    <ul v-for="user in listUser ":key="user.id">
        <li>
            <span>id: {{ user.id }}</span>
            <span>name: {{ user.name }}</span>
        </li>
    </ul>
  </div>
</template>

<script  setup>
const listUser=[
    {
        id:1,
        name:"Hà "
    },
    {
        id:2,
        name:"Hà Huyền "
    },
    {
        id:3,
        name:"Hà Huyền Tranng"
    },
    
]
</script>

<style>

</style>