<template>
    <div>
        <h1>Hello, Vue 3!{{ h }}:{{ timer }}:{{ count }}</h1>
        
    </div>
</template>

<script setup>
import { ref } from 'vue'
const count = ref(0)
const timer =ref(0)
const h=ref(0)

    setInterval(() => {
    count.value++
    if (count.value > 60) {
        count.value = 0
        timer.value++
        if (timer.value > 60) {
            timer.value = 0
            h.value++
            if (h.value > 24) {
                h.value = 0
            }
        }
    }
}, 1000)
    






</script>

<style scoped>
h1 {
    color: #42b983;
}
</style>
