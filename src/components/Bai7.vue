<template>
  <div>
    <button :class="{bg:bgcolor, text:textcolor}"  v-if="isShow"  @click="handleButton1">button1</button>
    <button :class="{bg:bgcolor2, text:textcolor2}"  v-if="isShow" @click="handleButton2">button2</button>
    <button :class="{bg:bgcolor3, text:textcolor3}" v-if="isShow" @click="handleButton3">button3</button>
  </div>
</template>

<script  setup>
import { ref } from 'vue';
const isShow =ref(true)
const activeIndex = ref(1)
const bgcolor = ref(false)
const textcolor = ref(false)


const bgcolor2 = ref(false)
const textcolor2 = ref(false)

const bgcolor3 = ref(false)
const textcolor3 = ref(false)


const handleButton1=()=>{
   bgcolor.value =! bgcolor.value
   textcolor.value=! textcolor.value
   bgcolor2.value =false
   textcolor2.value=false
   bgcolor3.value =false
   textcolor3.value=false
}
const handleButton2=()=>{
   bgcolor2.value =!bgcolor2.value
   textcolor2.value=!textcolor2.value
   bgcolor3.value =false
   textcolor3.value=false
   bgcolor.value =false
   textcolor.value=false
   activeIndex.value=activeIndex.value=2
}
const handleButton3=()=>{
   bgcolor3.value =! bgcolor3.value 
   textcolor3.value=!textcolor3.value
   bgcolor.value =false
   textcolor.value=false
   bgcolor2.value =false
   textcolor2.value=false
   activeIndex.value=activeIndex.value=3

}
</script>

<style>
    .bg{
        background-color: red
    }
    .text{
        color: #fff;
    }
</style>