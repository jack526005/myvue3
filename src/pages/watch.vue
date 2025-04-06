<template>
    <input type="text" v-model="message" >
    <p>{{ message }}</p>

</template>

<script setup>
import {ref,watch} from 'vue'
let message=ref('请输入内容')
watch(message,(newVal,oldVal)=>{//对message进行监听
    return console.log(newVal,oldVal)
},{immediate:true})//immediate:true表示立即执行
window.message=message
</script>

<style>

</style>
