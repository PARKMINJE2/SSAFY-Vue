<template>
  <div>
    <h1>쇼핑 애플리케이션</h1>
    <ProductList 
      :products="products"
      @add-to-cart="addToCart" 
    />
    <p>총 가격: {{ totalPrice }}원</p>
    <h2>장바구니</h2>
    <Cart 
      :cart-items="cartItems"
      @remove-from-cart="removeFromCart"
    />
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
import ProductList from '@/components/ProductList.vue'
import Cart from '@/components/Cart.vue'

let id = 0

const products = ref([
  { id: id++, name: '사과', price: 1000 },
  { id: id++, name: '바나나', price: 1500 },
  { id: id++, name: '딸기', price: 2000 },
  { id: id++, name: '포도', price: 3000 },
  { id: id++, name: '복숭아', price: 2000 },
  { id: id++, name: '수박', price: 5000 }
])

const cartItems = ref([])

const addToCart = (product) => {
  const cartItem = cartItems.value.find(item => item.id === product.id)
  if (cartItem) {
    cartItem.quantity += 1
  } else {
    cartItems.value.push({ ...product, quantity: 1 })
  }
}

const removeFromCart = (productId) => {
  const cartItemIndex = cartItems.value.findIndex(item => item.id === productId)
  if (cartItemIndex !== -1) {
    if (cartItems.value[cartItemIndex].quantity > 1) {
      cartItems.value[cartItemIndex].quantity -= 1
    } else {
      cartItems.value.splice(cartItemIndex, 1)
    }
  }
}

const totalPrice = computed(() => {
  return cartItems.value.reduce((sum, item) => sum + item.price * item.quantity, 0)
})
</script>
