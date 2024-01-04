<script setup>
import { ref } from 'vue'
import dropdownStart from './dropdownStart.vue'

const openDropdown = ref(null)

const dropdownItems = [
  { title: 'Клавиатуры' },
  { title: 'Аксессуары' },
  { title: 'Бренды' },
  { title: 'Услуги' }
]

const toggleDropdown = (title) => {
  if (openDropdown.value === title) {
    openDropdown.value = null
  } else {
    openDropdown.value = title
  }
}
</script>

<template>
  <header>
    <div class="flex justify-between items-center py-4 px-10 border-b border-slate-300">
      <div class="flex items-center gap-4 p-4">
        <img src="/Logo4.png" alt="Logo" class="w-14" />
        <div>
          <h2 class="text-2xl font-bold uppercase">onButtonPress</h2>
          <p class="text-slate-400">Лучший дистрибьютер клавиатур в СНГ</p>
        </div>
      </div>

      <ul class="flex items-center gap-10">
        <li class="flex items-center gap-4 flex-row cursor-pointer hover:-translate-y-1 transition">
          <img src="/favorite.svg" alt="profile" class="w-10 h-10" />
        </li>

        <li
          class="flex items-center flex-row cursor-pointer text-teal-500 hover:-translate-y-1 transition hover:text-teal-600"
        >
          <img src="/profile.svg" alt="profile" class="w-10 h-10" />
          <span>YYrkovskii@mail.ru</span>
        </li>

        <li
          class="flex items-center gap-4 cursor-pointer text-teal-500 hover:-translate-y-1 transition hover:text-teal-600"
        >
          <img src="/shopping.svg" alt="profile" class="w-10 h-10" />
          <b>16990 руб.</b>
        </li>
      </ul>
    </div>
    <div class="flex flex-row justify-between container mx-auto px-6 gap-4 py-4 bg-gray-600">
      <dropdownStart
        v-for="item in dropdownItems"
        :key="item.title"
        :title="item.title"
        :isOpen="openDropdown === item.title"
        :toggleDropdown="() => toggleDropdown(item.title)"
      />
      <div class="flex gap-4">
        <select
          @change="onChangeSelect"
          class="py-2 px-3 border-2 rounded-md outline-none bg-gray-600 text-white"
        >
          <option value="name">По названию</option>
          <option value="-price">По цене(Сначала дорогие)</option>
          <option value="price">По цене(Сначала дешевые)</option>
        </select>

        <div class="relative">
          <img class="absolute top-3 left-3" src="/search.svg" />
          <input
            @input="onChangeSearchInput"
            class="border rounded-md pl-11 pr-4 py-2 outline-none focus:border-gray-400"
            type="text"
            placeholder="Поиск..."
          />
        </div>
      </div>
    </div>
  </header>
</template>
