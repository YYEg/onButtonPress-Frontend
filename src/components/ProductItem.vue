<script setup>
defineProps({
  title: String,
  price: Number,
  isAvailable: Boolean,
  imageUrl: String
})
</script>

<template>
  <div>
    <div class="bg-white p-8 border-b border-slate-300 rounded-xl">
      <p class="border border-teal-500 text-teal-500 px-4 py-1 rounded-full w-fit">В наличии</p>
      <img :src="imageUrl" alt="Keybord" />
      <div class="flex justify-between">
        <div>
          <h1 class="font-bold">{{ title }}</h1>
          <p>{{ price }}</p>
        </div>
        <img src="/plus.svg" alt="plus" />
      </div>
    </div>
  </div>
</template>
