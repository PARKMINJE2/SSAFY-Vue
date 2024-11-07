<template>
    <div>
        <li>{{ myProduct.name }} - {{ myProduct.price }}원</li>
    </div>
</template>

<script setup>
defineProps({
    myProduct: Object
})
</script>

<style scoped>

</style>