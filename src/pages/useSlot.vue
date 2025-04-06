<template>
<myButton >
    12
   <template v-slot:button>点击</template> 
    <template v-slot:p>hello</template>
    
</myButton>
<myButton v-slot="scope">
    <p>{{scope.message}}</p>
    

</myButton>
<myButton v-slot="{message}">
    <p>{{message}}</p>
</myButton>
<myButton>
    <template #button="{message}">
        <button>{{message}}</button>
    </template>
</myButton>
</template>

<script setup>
import myButton from './myButton.vue'
</script>