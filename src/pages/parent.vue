<template>
    <div>父组件</div><hr>
    <chilren></chilren>
</template>
<script setup>
import { ref, useTemplateRef, onMounted } from 'vue';
import chilren from './chilren.vue';

</script>