<script setup></script>

<template>
  <div class="w-4/5 m-auto bg-slate-200 h-screen rounded-3xl shadow-2xl mt-2">
    <header class="flex justify-between items-center py-4 px-10 border-b border-slate-300">
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
    </header>
    <h1>Hello</h1>
  </div>
</template>
