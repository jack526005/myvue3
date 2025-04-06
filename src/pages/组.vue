<script setup>
const props=defineProps({title:{type:String,required:true},num:{type:Number,default:9, validator: (value) => {
      return value>=0;}}})

</script>

<template>
  <h4>{{ title }}</h4>
  <h3>{{num}}</h3>
 
</template>