<template>
  {{ data }}
</template>

<script setup lang="ts">
    // nuxt 3.1.2だと動かない
const { data } = await useAsyncData(() => $fetch('https://jsonplaceholder.typicode.com/posts/'))
const tes = await useAsyncData(() => $fetch('https://jsonplaceholder.typicode.com/posts/'))

console.log(data.value)
console.log(tes.data.value)
</script>

<!-- <script setup>
const { data: post } = await useFetch("https://pokeapi.co/api/v2/pokemon/1")
console.log(post.value) // script 内では .value をつける

</script> -->

<!-- <script setup lang="ts">
const test = await useFetch('https://jsonplaceholder.typicode.com/posts/');

const test2 = await useFetch('https://jsonplaceholder.typicode.com/posts/');

console.log(test.data)
console.log(test2.data)

console.log(test.data.value)
console.log(test2.data.value)

</script> -->



<!-- <script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  async setup() {
    const test1: any = await useAsyncData(() => $fetch('https://jsonplaceholder.typicode.com/posts/'))
    const test2: any = await useAsyncData(() => $fetch('https://jsonplaceholder.typicode.com/posts/'))

    console.log("1",test1.data.value)
    console.log("2",test2.data.value)

    return {
      test1,
      test2,
    }
  },
})
</script> -->

<!-- <script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  async setup() {
    const test1: any = await useAsyncData(() => $fetch('https://jsonplaceholder.typicode.com/posts/'))
    const test2: any = await useAsyncData(() => $fetch('https://jsonplaceholder.typicode.com/posts/'))

    console.log("1", test1.data.value)
    console.log("2", test2.data.value)


    // const shops:any = ref()
    // const { data: shopsData }:any = await useFetch('http://localhost:8080/albums')
    // console.log(shopsData)
    // shops.value = shopsData.value
    // console.log(shops.value)

    return {
      test1,
      test2,
    }
  },
})
</script> -->
