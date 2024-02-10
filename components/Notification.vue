<template>
  <div class="relative cursor-pointer">
    <Icon name="solar:bell-linear" class="text-2xl text-gray-500" />

    <div
      class="absolute -top-2 -right-2 w-[18px] h-[18px] bg-indigo-800 text-white flex justify-center items-center text-xs rounded-full"
    >
      {{ notificationItems }}
    </div>
  </div>
</template>

<script setup lang="ts">
const notificationItems = ref(9);
</script>
