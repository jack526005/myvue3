<template>
    <!-- 绑定字符串类名 -->
    <div :class="className">字符串语法</div>
    <!-- 对象语法 -->
    <div class="box2" :class="{ active: isActive, 'text-danger': hasError }">对象语法</div>
    <!-- 数组语法 -->
    <div :class="classArray">数组语法</div>
    <!-- 计算属性 -->
    <div :class="classComputed">计算属性</div>
</template>

<script setup>
import { ref, reactive, computed } from 'vue';

// 绑定字符串类名
let className = 'box'; // 修正拼写错误

// 对象语法
let isActive = ref(true);
let hasError = ref(false);

// 数组语法
let classArray = ['box', 'box2']; // 改为数组形式

// 计算属性
let classComputed = computed(() => {
    return { box: true, 'box2': true };
});
</script>

<style>
.box {
    border: 1px solid red;
}
.box2 {
    border: 1px solid green;
}
.active {
    color: blue;
}
.text-danger {
    color: red;
}
</style>