<template>
    {{ post }}
</template>
  
<script setup lang="ts">
const { data: post } = await useAsyncData(() => $fetch('https://jsonplaceholder.typicode.com/posts/'))

console.log(post.value)
</script>
