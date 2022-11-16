<script setup>
import { watchEffect } from 'vue';
  const emit = defineEmits(['passing'])

  const data = await fetch('https://fakestoreapi.com/products/1')
  const result = await data.json()

  const passData = () => {
    emit('passing', result)
  }

  watchEffect(() => {
    passData()
  })
</script>

<template>
  <div class="head">
    <div class="icon-img">
      <span class="profile">P</span>
      <span>Powdur</span>
    </div>
  </div>

  <div class="detail-item">
    <p class="type">{{result.title}}</p>
    <h4 class="price">${{result.price}}</h4>
    <div class="img-item">
      <img :src="result.image" width="200" alt="">
    </div>
  </div>
</template>

<style scoped>
.head {
  margin-bottom: 30px;
}

.profile {
  padding: 6px 10px;
  background-color: black;
  color: white;
  border-radius: 100px;
  margin-right: 5px;
}

.type {
  font-size: 14px;
  font-weight: bold;
  color: rgb(107, 107, 107);
}

.price {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 25px;
}

.img-item {
  box-shadow: 0px 10px 10px rgb(213, 213, 213);
  border-radius: 20px;
  padding: 20px;
  text-align: center;
}
</style>