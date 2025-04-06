<template>
  <div>
    <h1>标题</h1>
    <C title="123"></C>
    <C title="1000"></C>
    <C title="2000"></C>
    
    <C v-for="(item,index) in obj" title="3000" :name="item.name"></C>
  </div>
</template>

<script setup>
import { ref, useTemplateRef, onMounted } from 'vue';
import C from './C.vue';  
const obj=ref([{
      name: '李白'
    },{
      name: '王伟'
    }]);
</script>