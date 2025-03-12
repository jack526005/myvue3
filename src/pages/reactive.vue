<template>
    {{ message.name }}
</template>

<script setup>
import { reactive } from 'vue'
let message=reactive({name:'受命于天'})//只能是对象或数组类型的值

setTimeout(() => {
  message.name = '既寿永昌'
}, 5000)

</script>

<style >
</style>
