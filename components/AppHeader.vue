<template>
    <header class="flex justify-between border-b px-10">
      <div class="flex items-center gap-64">
        <ul class="flex items-center gap-8 text-gray-500">
          <img class="w-10 h-10" src="/logo1.png" alt="logo" />
          <li class="hover:text-black"><a href="#">Главная</a></li>
          <li class="hover:text-black"><a href="#">Программы обучения</a></li>
          <li class="hover:text-black"><a href="#">Курсы онлайн</a></li>
          <li class="hover:text-black"><a href="#">Документы</a></li>
        </ul>
  
        <div class="relative">
          <ul
            class="flex gap-1 text-gray-500 items-center cursor-pointer"
            @click="toggleDropdown"
          >
            <li class="hover:text-black"><img src="/Vector.svg" alt="" /></li>
            <li class="hover:text-black">Личный кабинет</li>
            <li class="hover:text-black"><img src="/Vector1.svg" alt="" /></li>
          </ul>
          <ul
            v-show="dropdownVisible"
            class="absolute bg-white shadow-lg border mt-2 rounded-lg text-sm text-gray-700 w-48"
          >
            <li class="hover:bg-gray-100 p-2"><a href="#">Обучение</a></li>
            <li class="hover:bg-gray-100 p-2"><a href="#">Курсы</a></li>
            <li class="hover:bg-gray-100 p-2"><a href="#">Расписание</a></li>
            <li class="hover:bg-gray-100 p-2"><a href="#">Портфолио</a></li>
          </ul>
        </div>
      </div>
    </header>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const dropdownVisible = ref(false)
  
  const toggleDropdown = () => {
    dropdownVisible.value = !dropdownVisible.value
  }
  </script>
  