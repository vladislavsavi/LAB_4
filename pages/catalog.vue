<script setup lang="ts">
const catalogItems = [{
  name: 'Cat\'s shit' ,
  weight: '100',
  taste: 'С орешками',
  price: '700'
}, {
  name: 'Bull\'s shit' ,
  weight: '1000',
  taste: 'Не очень',
  price: '1000'
}]
</script>

<template>
<div class="container">
  <h1>Каталог</h1>
  <div v-for="(item, index) in catalogItems" :key="index" class="item">
    <div class="item-content">
      <img alt="bla-bla" src="https://via.placeholder.com/100x100" />
      <div>
        <h3>{{item.name}}</h3>
        <p>Объем: {{item.weight}}</p>
        <p>Вкус: {{item.taste}}</p>
        <p>Цена: {{item.price}}</p>
      </div>
    </div>
    <button>Навернуть</button>
  </div>
</div>
</template>

<style scoped>
.item-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.item {
  button {
    width: 100%;
    padding: 8px 16px;
    border: none;
    background-color: green;
    color: #fff;
  }
}
</style>
