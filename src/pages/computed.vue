<template>
    <p>Has published books:</p>
    <span>{{ time }}</span>
    <p>{{ fullname }}</p>
    <p>{{ fullnameChange }}</p>
    

</template>

<script setup>
import {ref,computed,reactive} from 'vue'

let time= computed(() => {//定义相同的函数，计算属性只会在数据改变时才更新
   return Date.now()
}
)
let time2=function(){
    return Date.now()
}
let firstname=ref('李')
let lastname=ref('白')
let fullname=computed(()=>{//计算属性只有在相关依赖发生改变时才会重新求值
    return firstname.value+lastname.value
})
let fullnameChange=computed({//更改计算属性的值
    get(){
        return firstname.value+''+lastname.value
    },
    set(newValue) {//输入的新值用空格间隔
    // 注意：我们这里使用的是解构赋值语法
    [firstname.value, lastname.value] = newValue.split(' ')
  }
})
   

window.time=time
window.time2=time2
window.fullname=fullname
window.firstname=firstname
window.lastname=lastname
window.fullnameChange=fullnameChange

</script>

<style>

</style>