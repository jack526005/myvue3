<template>
<p v-for="item in obj">{{ item.name }}{{ item.age }}</p>
<el-button type="warn">Primary Button</el-button>
</template>
<script setup>
import { ref, reactive } from 'vue';
let list = reactive([1, 2, 3, 4, 5]);
let arr = reactive(['苹果', '香蕉', '橘子']);
let obj = reactive([{ name: '张三', age: 18 },{ name: '李四', age: 20 },{ name: '王五', age: 22 }]);

</script>

<style>

</style>