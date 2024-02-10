<template>
  <div class="relative cursor-pointer">
    <Icon
      name="solar:folder-favourite-star-linear"
      class="text-2xl text-gray-500"
    />

    <div
      class="absolute -top-2 -right-1 w-[18px] h-[18px] bg-indigo-800 text-white flex justify-center items-center text-xs rounded-full"
    >
      {{ wishlistItems }}
    </div>
  </div>
</template>

<script setup lang="ts">
const wishlistItems = ref(9);
</script>
