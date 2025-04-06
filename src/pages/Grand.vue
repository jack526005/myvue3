<template>
    <div>爷爷组件</div>
    <hr>
    <parent></parent>
</template>
<script setup>
import { ref, useTemplateRef, onMounted, provide } from 'vue';
import parent from './parent.vue';
let money=ref(1000)
let updatemonet=(value)=>{
    money.value+=value
}
provide('money',money)//提供数据
provide('updatemonet',updatemonet)//提供方法
</script>