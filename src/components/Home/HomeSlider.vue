<script setup>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'

let ElSwiper = ref(null)

const onSwiper = (swiper) => {
  ElSwiper = swiper
}

let currentSlide = ref(0)
const onSlideChange = () => {
  // eslint-disable-next-line vue/no-ref-as-operand
  currentSlide.value = ElSwiper.activeIndex
}

const slideTo = (slideNumber) => {
  // eslint-disable-next-line vue/no-ref-as-operand
  ElSwiper.slideTo(slideNumber)
}

const prevSlide = () => {
  if(currentSlide.value == 0) return
  slideTo(currentSlide.value - 1)
}

const nextSlide = () => {
  if(currentSlide.value == 2) return
  slideTo(currentSlide.value + 1)
}
</script>


<template>
  <div class="w-full h-[439px] lg:h-[576px] relative">
    <swiper
      ref="ssswiper"
      class="w-full h-full"
      :slides-per-view="1"
      :space-between="0"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <swiper-slide>
        <div class="slide-1 w-full h-full text-white px-[24px] lg:px-[128px]">
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
      </swiper-slide>

      <swiper-slide>
        <div class="slide-2 w-full h-full text-white px-[24px] lg:px-[128px]">
          <div class="container mx-auto max-w-[1280px] pt-[30px] lg:pt-[80px] h-full flex flex-col justify-between pb-[20px] lg:pb-[70px]">
            <div class="">
              <div class="uppercase bg-white flex px-[10px] py-[7px] inline-flex justify-center items-center rounded-[13px] text-[9px] font-extrabold text-[#111721]">
                nike
              </div>
              <div class="mt-[35px] font-medium text-[14px] leading-[21px]">
                Твоё воображение — место твоей<br> силы, у которой нет границ
              </div>
            </div>

            <div class="">
              <div class="font-bold text-[28px] lg:text-[48px]">
                Твоя суперсила<br> — это твоя цель
              </div>

              <a href="" class="flex mt-[28px] lg:mt-[20px] items-center text-white">
                Выбрать <img src="@/assets/img/arrow-right.svg" class="ml-[5px]" alt="arrow-right">
              </a>
            </div>
          </div>
        </div>
      </swiper-slide>

      <swiper-slide>
        <div class="slide-1 w-full h-full text-white px-[24px] lg:px-[128px]">
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
      </swiper-slide>
    </swiper>

    <div class="hidden lg:flex absolute bottom-[24px] w-full justify-center items-center z-99 space-x-[20px]">
      <div class="w-[8px] h-[8px] bg-[#303748] rounded-full transition-colors cursor-pointer" :class="{ 'bg-white': currentSlide == 0}" @click="slideTo(0)" />
      <div class="w-[8px] h-[8px] bg-[#303748] rounded-full transition-colors cursor-pointer" :class="{ 'bg-white': currentSlide == 1}" @click="slideTo(1)" />
      <div class="w-[8px] h-[8px] bg-[#303748] rounded-full transition-colors cursor-pointer" :class="{ 'bg-white': currentSlide == 2}" @click="slideTo(2)" />
    </div>

    <div class="hidden lg:flex left-[0%] transform px-[65px] xl:px-[128px] absolute top-[50%] translate-y-[-50%] justify-between items-center z-1">
      <svg class="cursor-pointer transition-opacity" :class="{ 'opacity-20': currentSlide == 0 }" width="56" height="56" viewBox="0 0 56 56" fill="none" xmlns="http://www.w3.org/2000/svg" @click="prevSlide()">
        <path d="M28 51.3333C15.134 51.3333 4.66667 40.866 4.66667 28C4.66667 15.134 15.134 4.66666 28 4.66667C40.866 4.66667 51.3333 15.134 51.3333 28C51.3333 40.866 40.866 51.3333 28 51.3333ZM28 56C43.463 56 56 43.463 56 28C56 12.537 43.463 8.11329e-07 28 -5.40489e-07C12.537 -1.89231e-06 5.707e-06 12.537 4.35519e-06 28C3.00337e-06 43.463 12.537 56 28 56ZM23.3333 28L33.8333 17.5L30.2703 14L16.3333 28L30.2703 42L33.8333 38.5L23.3333 28V28Z" fill="white" />
      </svg>
    </div>

    <div class="hidden lg:flex right-[0%] transform px-[65px] xl:px-[128px] absolute top-[50%] translate-y-[-50%] justify-between items-center z-1">
      <svg class="cursor-pointer transition-opacity" :class="{ 'opacity-20': currentSlide == 2 }" width="56" height="56" viewBox="0 0 56 56" fill="none" xmlns="http://www.w3.org/2000/svg" @click="nextSlide()">
        <path d="M28 4.66667C40.866 4.66667 51.3333 15.134 51.3333 28C51.3333 40.866 40.866 51.3333 28 51.3333C15.134 51.3333 4.66667 40.866 4.66667 28C4.66667 15.134 15.134 4.66667 28 4.66667ZM28 0C12.537 0 0 12.537 0 28C0 43.463 12.537 56 28 56C43.463 56 56 43.463 56 28C56 12.537 43.463 0 28 0ZM32.6667 28L22.1667 38.5L25.7297 42L39.6667 28L25.7297 14L22.1667 17.5L32.6667 28Z" fill="white" />
      </svg>
    </div>
  </div>
  <div class="flex lg:hidden w-full mt-[23px] justify-center items-center z-99 space-x-[20px]">
    <div class="w-[8px] h-[8px] border-[#C63434] border-[1px] rounded-full transition-colors cursor-pointer" :class="{ 'bg-white': currentSlide == 0, 'bg-[#C63434]': currentSlide != 0}" @click="slideTo(0)" />
    <div class="w-[8px] h-[8px] border-[#C63434] border-[1px] rounded-full transition-colors cursor-pointer" :class="{ 'bg-white': currentSlide == 1, 'bg-[#C63434]': currentSlide != 1}" @click="slideTo(1)" />
    <div class="w-[8px] h-[8px] border-[#C63434] border-[1px] rounded-full transition-colors cursor-pointer" :class="{ 'bg-white': currentSlide == 2, 'bg-[#C63434]': currentSlide != 2}" @click="slideTo(2)" />
  </div>
</template>

<style lang="scss" scoped>
.slide-1 {
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.1806) 0%, rgba(0, 0, 0, 0.48) 99.99%, rgba(0, 0, 0, 0.48) 100%), url('@/assets/img/slide-1.jpg');
  background-size: cover;
  background-position: center;
}

.slide-2 {
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.1806) 0%, rgba(0, 0, 0, 0.48) 99.99%, rgba(0, 0, 0, 0.48) 100%), url('@/assets/img/slide-2.jpg');
  background-size: cover;
  background-position: center;
}
</style>
