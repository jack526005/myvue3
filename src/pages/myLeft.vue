<template>
    <div>
        <h1>My Left Component</h1>
        <p>This is the left component of the layout.</p>
    </div>
</template>
<script setup>

import {onMounted, onUnmounted} from 'vue'
onMounted(() => {
    console.log("Left组件挂载")
})

onUnmounted(() => {
    console.log("Left组件卸载")
})

</script>