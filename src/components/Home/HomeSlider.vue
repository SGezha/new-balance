<template>
  <div class="slide-1 w-full h-[439px] lg:h-[576px] text-white px-[24px] lg:px-[128px]">
    <div class="container mx-auto max-w-[1280px] pt-[30px] lg:pt-[80px] h-full flex flex-col justify-between pb-[20px] lg:pb-[70px]">
      <div class="">
        <div class="uppercase bg-white flex px-[10px] py-[7px] inline-flex justify-center items-center rounded-[13px] text-[9px] font-extrabold text-[#111721]">
          adidas
        </div>
        <div class="mt-[35px] font-medium text-[14px] leading-[21px]">
          Твоё воображение — место твоей<br> силы, у которой нет границ
        </div>
      </div>

      <div class="">
        <div class="font-bold text-[28px] lg:text-[48px]">
          Выбери свою игру
        </div>

        <a href="" class="flex mt-[28px] lg:mt-[20px] items-center text-white">
          Выбрать <img src="@/assets/img/arrow-right.svg" class="ml-[5px]" alt="arrow-right">
        </a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.slide-1 {
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.1806) 0%, rgba(0, 0, 0, 0.48) 99.99%, rgba(0, 0, 0, 0.48) 100%), url('@/assets/img/slide-1.jpg');
  background-size: cover;
  background-position: center;
}
</style>
