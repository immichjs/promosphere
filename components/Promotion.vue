<template>
  <section class="h-10 flex items-center justify-center bg-indigo-800">
    <div class="container flex items-center justify-center">
      <p class="text-white font-medium text-sm">
        {{ description }}
      </p>
    </div>
  </section>
</template>

<script setup lang="ts">
const description = ref(
  "🔥 Por tempo limitado! Aproveite descontos exclusivos."
);
</script>
