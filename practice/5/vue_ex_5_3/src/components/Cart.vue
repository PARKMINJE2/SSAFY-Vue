<template>
    <div v-if="cartItems.length > 0">
        <ul>
            <li v-for="item in cartItems" :key="item.id">
                {{ item.name }} x {{ item.quantity }}
                <button @click="$emit('remove-from-cart', item.id)">삭제</button>
            </li>
        </ul>
    </div>
    <p v-else>장바구니에 제품이 없습니다.</p>
</template>
  
<script setup>
import { defineProps, defineEmits } from 'vue'

defineProps({
    cartItems: Array
})
  

const emit = defineEmits()
  

const removeFromCart = (productId) => {
    emit('remove-from-cart', productId)
    }
</script>
  