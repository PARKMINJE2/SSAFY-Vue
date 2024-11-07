<template>
  <div>
    <header>
      <h1 class="title">My Gallery</h1>
    </header>

    <main class="container">
      <div class="row">
        <div
          class="col-12 col-sm-6 col-md-4 mb-4"
          v-for="item in numberOfItems"
          :key="item"
        >
          <div class="card" style="width: 100%;">
            <img src="@/assets/sample.png" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">
                Some quick example text to build on the card title and make up the bulk of the card's content.
              </p>
              <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const numberOfItems = ref(4)
</script>

<style scoped>
.title {
  position: fixed;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  text-align: center;
  padding: 20px 0;
  background-color: #b3dbd0;
  z-index: 1000;
}

.container {
  margin-top: 100px;
}
</style>
