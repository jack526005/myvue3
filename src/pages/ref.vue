<template>
  {{message  }}
</template>

<script setup>
//time
import { ref } from 'vue'
let message = ref('受命于天')//几乎可以是任何类型的值
setTimeout(() => {
  message.value = '既寿永昌'
}, 5000)
window.message = message//win11如果注释会出现问题，无法改变value







</script>

<style >
h1 {
    color: #42b983;
}
</style>
