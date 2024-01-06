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
    <div
      class="bg-white p-8 border-b border-slate-300 rounded-xl hover:-translate-y-2 hover:scale-105 hover:shadow-2xl transition"
    >
      <p
        v-if="isAvailable"
        class="border border-teal-500 text-teal-500 px-4 py-1 rounded-full w-fit"
      >
        В наличии
      </p>
      <p
        v-if="!isAvailable"
        class="border border-pink-500 text-pink-500 px-4 py-1 rounded-full w-fit"
      >
        Нет в наличии
      </p>
      <img src="/keyboards/large_87.jpg" alt="Keybord" />
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
