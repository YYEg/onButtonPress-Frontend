<script setup>
import ProductItem from './ProductItem.vue'

defineProps({
  products: Array
})
</script>

<template>
  <div class="mt-10 p-10">
    <div class="grid grid-cols-3 gap-4">
      <ProductItem
        v-for="product in products"
        :key="product.id"
        :title="product.title"
        :imageUrl="product.imageUrl"
        :price="product.price"
        :isAvailable="product.isAvailable"
      />
    </div>
  </div>
</template>
