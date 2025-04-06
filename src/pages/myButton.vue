<template>
    这是插槽
    <slot></slot>
<button>
    <slot name="button" message="这是button"></slot>
</button>
<p><slot name="p"></slot></p>
<div>
    <slot message="hello vue.js"></slot>
</div>
    


</template>
