<template>
  <div class="greeting">
    {{ msg }}
  </div>
</template>

<!-- Vue CDN 불필요 -->
<!-- ↓setup 함수 -->
<script setup>
// const { ref } = Vue
import { ref } from 'vue'

const msg = ref('Hello World!')
// return 작성 불필요
</script>

<style scoped>
.greeting {
  color: red;
}
</style>