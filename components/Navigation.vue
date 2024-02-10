<template>
  <nav class="hidden gap-8 xl:flex">
    <NuxtLink
      :to="navigationItem.redirectTo"
      v-for="navigationItem in navigationItems"
      class="text-sm text-zinc-700 hover:text-indigo-800"
    >
      {{ navigationItem.label }}
    </NuxtLink>
  </nav>
</template>

<script setup lang="ts">
const navigationItems = ref([
  { redirectTo: "promotions", label: "Promoções" },
  { redirectTo: "best-sellers", label: "Mais vendidos" },
  { redirectTo: "categories", label: "Categorias" },
  { redirectTo: "about-us", label: "Sobre nós" },
]);
</script>
