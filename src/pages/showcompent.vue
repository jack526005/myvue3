<template>
<button @click="showCompent=myLeft">left组件</button>
<button @click="showCompent=myRight">right组件</button>
<div>
    
         <component :is="showCompent"></component>
    
   
</div>
</template>
<script setup >
import myLeft from './myLeft.vue'
import myRight from './myRight.vue'
import { shallowRef } from 'vue'
const showCompent=shallowRef(myLeft)//动态组件

</script>