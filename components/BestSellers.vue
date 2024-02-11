<template>
  <section class="mt-12 w-full xl:max-w-[1280px]">
    <div class="flex justify-between items-center">
      <div class="flex gap-4">
        <h2 class="text-md">Mais vendidos</h2>
        <button class="text-[0.65rem] underline text-zinc-400">
          Ver todos
        </button>
      </div>

      <div class="flex items-center gap-2">
        <button
          class="w-8 h-8 flex justify-center items-center bg-white border border-zinc-200 shadow-sm text-toro-800 rounded-full text-lg"
        >
          <Icon name="i-solar:alt-arrow-left-outline" />
        </button>
        <button
          class="w-8 h-8 flex justify-center items-center bg-white border border-zinc-200 shadow-sm text-toro-800 rounded-full text-lg"
        >
          <Icon name="i-solar:alt-arrow-right-outline" />
        </button>
      </div>
    </div>
    <div class="grid grid-cols-4 gap-4 mt-4">
      <div class="border rounded-[1.5rem] p-4 shadow" v-for="i in 4">
        <div class="overflow-hidden flex justify-center">
          <img src="https://picsum.photos/400/400" class="rounded-xl" alt="" />
        </div>

        <div class="mt-2">
          <h2>RJ - Tijuca</h2>
          <p class="text-xs font-light">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Natus
            perferendis unde omnis?
          </p>
        </div>

        <div class="flex justify-between mt-4">
          <div class="flex flex-col">
            <span class="text-xs text-zinc-500 font-light">A partir de:</span>
            <span class="text-xl font-semibold text-toro-800">R$ 19,90</span>
          </div>

          <button
            class="bg-toro-800 text-white px-4 py-2.5 flex items-center gap-2 rounded-xl text-sm"
          >
            Ir até a loja
            <Icon name="i-solar:rocket-outline" class="text-xl" />
          </button>
        </div>
      </div>
    </div>
  </section>
</template>
