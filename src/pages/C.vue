<template>
    
  
    
    <p>count的值为：{{ count }}</p>
    <button @click="add">加n</button><!--触发事件-->
  </template>
  
  <script setup> 
  // 这里可以添加 C 组件的逻辑
  import { ref} from 'vue'
  
const emit = defineEmits(['updateCount'])//声明事件
const count=ref(1)
const add = () => {
  count.value++ 
  emit('updateCount', 2)
}
  </script>
  <style>

</style>