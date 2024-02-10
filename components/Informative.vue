<template>
  <section class="w-full max-w-[1024px] grid lg:grid-cols-4 my-24 gap-8">
    <div
      class="flex gap-4 items-center"
      v-for="informativeItem in informativeItems"
    >
      <Icon :name="informativeItem.icon" class="text-5xl text-indigo-800" />

      <p class="text-sm">
        <strong>{{ informativeItem.label }}</strong> {{ informativeItem.text }}
      </p>
    </div>
  </section>
</template>

<script setup lang="ts">
const informativeItems = ref([
  {
    icon: "solar:cart-large-minimalistic-linear",
    label: "Envio rápido e garantido.",
    text: "para todo Brasil",
  },
  {
    icon: "solar:card-linear",
    label: "Parcele suas compras",
    text: "com cartão de crédito",
  },
  {
    icon: "solar:lock-password-outline",
    label: "Loja confiável",
    text: "com tecnologia 100% segura",
  },
  {
    icon: "solar:refresh-outline",
    label: "Troque e devolva",
    text: "seus produtos em até 30 dias",
  },
]);
</script>
