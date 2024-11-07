<template>
  <li>
    {{ myProduct.name }} - {{ myProduct.price }}원
    <button @click="addDarai">장바구니에 추가</button>
  </li>
</template>

<script setup>
defineProps({
  myProduct: Object
})

const emit = defineEmits(['addDarai'])

const addDarai = () => {
  emit('addDarai')
}
</script>
