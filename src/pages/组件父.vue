<script setup>
import { ref } from 'vue'
import BlogPost from './BlogPost.vue'
  
const posts = ref([
  { id: 1, title: 'My journey with Vue' ,num:3},
  { id: 2, title: 'Blogging with Vue'},
  { id: 3, title: 'Why Vue is so fun',num:1}
])
</script>

<template>
	<BlogPost
  	v-for="post in posts"
	  :key="post.id"
  	:title="post.title"
		:num="post.num"
	></BlogPost>
</template>