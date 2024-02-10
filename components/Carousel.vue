<template>
  <section
    class="w-full lg:max-w-[1280px] container overflow-hidden relative rounded-[2.5rem]"
  >
    <Swiper
      class="swiper-container"
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

      <SwiperSlide v-for="slide in 5" :key="slide">
        <div
          class="flex items-center justify-center h-full"
          :style="{ background: generateHexColor() }"
        >
          <span class="text-white text-3xl">Slide {{ slide }}</span>
        </div>
      </SwiperSlide>
    </Swiper>
  </section>
</template>

<script setup lang="ts">
const modules = [
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

function generateHexColor() {
  const r = Math.floor(Math.random() * 256);
  const g = Math.floor(Math.random() * 256);
  const b = Math.floor(Math.random() * 256);

  const corHex = `#${r.toString(16).padStart(2, "0")}${g
    .toString(16)
    .padStart(2, "0")}${b.toString(16).padStart(2, "0")}`;

  return corHex;
}
</script>

<style>
.swiper-container {
  width: 100%;
  height: 490px;
  overflow: hidden;
  border-radius: 40px;
}

.swiper-slide {
  height: 100%;
}

.swiper-button-prev {
  left: 64px;
}

.swiper-button-next {
  right: 64px;
}

.swiper-button-prev,
.swiper-button-next {
  background-color: #fff;
  width: 3rem;
  height: 3rem;
  border-radius: 9999px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  @apply text-indigo-800;
}

.swiper-button-prev::after,
.swiper-button-next::after {
  display: none;
}

.swiper-pagination-bullet-active {
  @apply bg-indigo-800;
}
</style>
