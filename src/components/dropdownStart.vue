<script setup>
defineProps({
  title: String,
  isOpen: Boolean,
  toggleDropdown: Function
})
</script>

<template>
  <div class="relative text-left inline-flex flex-col">
    <button
      class="p-3 bg-gray-600 text-white flex items-center gap-2 hover:text-gray-400 transition"
      @click="toggleDropdown"
    >
      {{ title }}
      <img src="/arrow-right.svg" alt="search" class="w-5 h-5" :class="{ 'rotate-90': isOpen }" />
    </button>
    <div v-if="isOpen" class="absolute w-full mt-12 bg-gray-600 text-white">
      <a class="block p-3 hover:bg-gray-800 transition" href="#">Link2</a>
      <a class="block p-3 hover:bg-gray-800 transition" href="#">Link3</a>
      <a class="block p-3 hover:bg-gray-800 transition" href="#">Link1</a>
    </div>
  </div>
</template>
