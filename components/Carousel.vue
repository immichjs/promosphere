<template>
  <section
    class="w-full lg:max-w-[1280px] container overflow-hidden relative rounded-[2rem]"
  >
    <Swiper
      class="h-[200px] w-full rounded-3xl"
      :modules="modules"
      :slides-per-view="1"
      :pagination="pagination"
      :navigation="navigation"
      :autoplay="autoplay"
      :loop="true"
    >
      <div class="swiper-button-prev">
        <button class="text-2xl">
          <Icon name="iconamoon:arrow-left-2-bold" />
        </button>
      </div>
      <div class="swiper-button-next">
        <button class="text-2xl">
          <Icon name="iconamoon:arrow-right-2-bold" />
        </button>
      </div>

      <SwiperSlide v-for="slide in 5" :key="slide" class="h-full">
        <div class="flex items-center justify-center h-full bg-violet-800">
          <span class="text-white text-3xl">Slide {{ slide }}</span>
        </div>
      </SwiperSlide>
    </Swiper>
  </section>
</template>

<script setup lang="ts">
import type { ModuleOptions } from "nuxt-swiper";

const modules: ModuleOptions[] = [
  SwiperAutoplay,
  SwiperEffectCreative,
  SwiperNavigation,
  SwiperPagination,
];
const pagination = {
  clickable: true,
  enabled: true,
  dynamicBullets: true,
};
const navigation = {
  enabled: true,
  nextEl: ".swiper-button-next",
  prevEl: ".swiper-button-prev",
};
const autoplay = {
  delay: 4000,
  disableOnInteraction: true,
};
</script>

<style scoped lang="postcss">
.swiper-button-prev {
  left: 64px;
}

.swiper-button-next {
  right: 64px;
}

.swiper-button-prev,
.swiper-button-next {
  @apply text-violet-800 shadow bg-white flex rounded-full items-center justify-center w-12 h-12 cursor-pointer;
}

.swiper-button-prev::after,
.swiper-button-next::after {
  display: none;
}
</style>
