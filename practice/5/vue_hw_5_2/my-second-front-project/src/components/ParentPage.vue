<template>
    <div>
        <h1>부모 페이지입니다.</h1>
        <ChildPage 
            v-for="children in childrens"
            :key="children.id"
            :my-children="children"
        />
    </div>
</template>

<script setup>
import ChildPage from '@/components/ChildPage.vue'
import { ref } from 'vue'

const childrens = ref([
    { name: '김하나', age: 30},
    { name: '김두리', age: 20},
    { name: '김서이', age: 10}
])

</script>

<style scoped>
div {
  border: 1px solid #ccc;
  padding: 10px;
  margin-top: 10px;
}
</style>