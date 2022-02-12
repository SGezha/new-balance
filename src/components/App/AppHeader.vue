<script setup>
import { ref } from 'vue'

const menu = ref(false)
</script>

<template>
  <header class="fixed w-full top-0 z-2 bg-[#fff] h-[60px] lg:h-[88px] overflow-hidden" :class="{ 'menu_shadow': !menu, 'h-[60px]': !menu, 'h-[500px]': menu }">
    <div class="container mx-auto px-[24px] h-[60px] lg:px-[30px] lg:h-[88px] flex items-center justify-between">
      <div class="lg:ml-[33px]">
        <img class="w-[53.5px] h-[30px] lg:h-[40px] lg:w-[80px]" src="@/assets/img/logo.png">
      </div>
      <div class="lg:hidden">
        <img v-if="!menu" src="@/assets/img/menu.svg" @click="menu = !menu">
        <img v-else src="@/assets/img/close.svg" @click="menu = !menu">
      </div>

      <div class="hidden lg:flex w-full ml-[88px] items-center justify-end space-x-[52px] text-center text-[#11172166] text-12px font-medium xl:text-[16px]">
        <a href="" class="text-[#111721] hover:text-[#111721] transition-colors">Главная</a>
        <a href="" class=" hover:text-[#111721] transition-colors">Отрасли применения</a>
        <a href="" class=" hover:text-[#111721] transition-colors">Возможности печати</a>
        <a href="" class=" hover:text-[#111721] transition-colors">Специальные предложения</a>
        <a href="" class=" hover:text-[#111721] transition-colors">Готовые штампы</a>
        <a href="" class=" hover:text-[#111721] transition-colors">Видео</a>
        <a href="" class=" hover:text-[#111721] transition-colors">Контакты</a>
      </div>
    </div>

    <div class="flex flex-col items-center justify-center mt-[60px] space-y-[21px] text-[20px] leading-[24px] text-[#11172166] font-medium">
      <a href="" class="text-[#111721]">Главная</a>
      <a href="">Отрасли применения</a>
      <a href="">Возможности печати</a>
      <a href="">Специальные предложения</a>
      <a href="">Готовые штампы</a>
      <a href="">Видео</a>
      <a href="">Контакты</a>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.menu_shadow {
  box-shadow: 0px 0.5px 0px rgba(36, 80, 154, 0.15);
}

header {
  transition: 0.5s ease-in-out;
}

</style>
