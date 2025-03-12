<template>
    <div v-text="message1"></div>
    <div v-html="message1"></div>
    <div>{{ message1 }}</div>
    <p><input type="text" v-bind:placeholder="username"></p>
    <p><input type="password" v-bind:placeholder="password"></p>
    <button @click="show" >登录</button>
    <p><input type="text" v-model="message2"> <span>{{ message2 }}</span></p>
    <p v-if="message3==='李白'">大河之水天上来</p>
    <p v-else>奔流到海不复回</p>
    <p v-show="message4==='杜甫'">大庇天下寒士俱欢颜</p>
    <p v-show="message4==='李白'">十步杀一人，千里不留行</p>
    <div v-for="item in message5">
        {{ item }}
    </div>

 
</template>
<script setup>
import {ref,reactive} from 'vue'
let message1 = '<span>受命于天,既寿永昌</span>'//v-text是vue3的指令,不解析html元素
 //v-html是vue3的指令,解析html元素
 let username='请输入用户名'//v-bind是vue3的指令,绑定属性
 let password='请输入密码'  //placeholder是html的属性,类似于hint提示
 let show=()=>{            //v-on是vue3的指令,绑定事件
     alert('点击了按钮')
     
 }
    let message2=ref('受命于天,既寿永昌')//v-model是vue3的指令,双向绑定，一定要用ref
    let message3=ref('李白')//v-if是vue3的指令,如果为真则显示
    let message4=ref('杜甫')//v-show是vue3的指令,如果为真则显示,和v-if的区别是v-if是删除节点,v-show是隐藏节点如果只进行一次操作,建议使用v-if，如果多次操作建议使用v-show
    let message5=reactive(['李白','杜甫','白居易'])//v-for是vue3的指令,循环数组或对象

</script>
<style>


</style>