<template>
    <div>子组件</div>
    <hr>
    <p>爷爷传过来的钱：{{ money }}</p>
    <button @click="updateMoney(500)">增加500</button>
    
</template>
<script setup>
import { inject } from 'vue';

let money=inject('money')//接收爷爷传过来的数据
let updateMoney=inject('updatemonet')//接收爷爷传过来的方法

</script>