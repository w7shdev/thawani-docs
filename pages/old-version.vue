<template>
   <div class="container mx-auto">
    <div class="py-8">
      <div class="flex">
        <div class="text-1xl tracking-wider">@Thawani node docs</div>
      </div>

      <div class="text-gray-500 mt-1 text-xs">
        This Documentation is to make the development process easier for you
      </div>

      <h1 class="text-1xl text-green-500">
          <nuxt-link to="/">Home page (newest version)</nuxt-link>
      </h1>
      <!-- here the seession documentation -->
     
        <nuxt-content
          :document="doc"
          class="prose p-2 max-w-none w-full my-8 mt-20 lg:prose-sm lg:w-2/3 lg:mx-auto lg:p-0"
        />
     
    </div>
    <div class="text-1xl tracking-wider py-4">Created by <a href="#">Muhannad</a> with 🔨 Nuxtjs & tailwindcss </div>
  </div>
</template>

<script>
export default {
    async asyncData({ $content, params }) {
    const doc = await $content("old-doc", 'index').fetch();
    return { doc };
  },
}
</script>