<template>
  <header
    class="flex justify-center h-20 bg-white py-2 box-border border-b px-8 xl:p-0"
  >
    <section class="w-full lg:max-w-[1200px] flex justify-between items-center">
      <div class="flex items-center gap-12">
        <Menu />
        <img src="~/assets/images/logo.png" class="w-12" />

        <Navigation />
      </div>

      <div class="flex items-center gap-6">
        <!-- <Search /> -->

        <div class="flex gap-6 items-center">
          <Notification />
          <Wishlist />
          <Profile />
        </div>
      </div>
    </section>
  </header>
</template>
