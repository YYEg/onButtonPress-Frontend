<script setup>
import Header from './components/HeaderMain.vue'
import ProductItemList from './components/ProductItemList.vue'

const products = [
  {
    id: 1,
    title: 'Varmilo Yakumo v2 87',
    price: 18490,
    isAvailable: true,
    imageUrl: 'keyboards/large_87.jpg'
  },
  {
    id: 2,
    title: 'Varmilo Yakumo v3 87',
    price: 16000,
    isAvailable: true,
    imageUrl: 'keyboards/large_87.jpg'
  },
  {
    id: 3,
    title: 'Varmilo Yakumo v4 87',
    price: 9900,
    isAvailable: true,
    imageUrl: 'keyboards/large_87.jpg'
  }
]
</script>

<template>
  <div class="w-5/6 m-auto bg-slate-200 shadow-2xl mt-2">
    <Header />
    <ProductItemList :products="products" />
  </div>
</template>
