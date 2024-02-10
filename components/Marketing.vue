<template>
  <section class="w-full lg:max-w-[1280px] grid grid-cols-3 gap-8">
    <div
      class="bg-indigo-800 rounded-[2.5rem] h-44 text-white text-xl flex justify-center items-center"
      v-for="i in 3"
    >
      Slide {{ i }}
    </div>
  </section>
</template>
