<template>
<p>父组件当前的值:{{ number }}</p>
<C @updateCount="updateEmitCoount"> </C><!--监听子组件的事件-->
</template>
<script setup>
import { ref, useTemplateRef, onMounted } from 'vue';
import C from './C.vue';
const number=ref(10)
const updateEmitCoount=(value)=>{
number.value+=value

}
</script>