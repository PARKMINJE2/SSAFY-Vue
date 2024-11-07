<template>
    <div>
        <h3>자식 페이지입니다.</h3>
        <p>{{ myChildren.name }}</p>
        <p>{{ myChildren.age }}</p>
    </div>
</template>

<script setup>
defineProps({
    myChildren: Object
})
</script>

<style scoped>

</style>