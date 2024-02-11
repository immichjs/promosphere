<template>
  <header
    class="flex justify-center h-20 bg-white py-2 box-border border-b px-4"
  >
    <section class="w-full lg:max-w-[1280px] flex justify-between items-center">
      <div class="flex items-center gap-12">
        <Menu />

        <Navigation />
      </div>

      <div class="flex items-center">
        <div class="flex gap-6 items-center">
          <Search />
          <Notification />
          <Wishlist />
          <Profile />
        </div>
      </div>
    </section>
  </header>
</template>
