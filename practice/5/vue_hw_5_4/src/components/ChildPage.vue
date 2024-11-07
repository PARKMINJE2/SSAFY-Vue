<template>
    <div>
        <h3>자식 페이지입니다.</h3>
        <p>이름: {{ myChildren.name }}</p>
        <p>나이: {{ myChildren.age }}</p>
        <p>용돈: {{ myChildren.balance }}</p>
        <button @click="updateBalance">용돈주세요.</button>
    </div>
</template>

<script setup>
defineProps({
    myChildren: Object
})

const emit = defineEmits(['update-balance'])

const updateBalance = () => {
    emit('update-balance')
}
</script>

<style scoped>

</style>