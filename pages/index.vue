<template>
  <div class="container mx-auto">
    <div class="py-8">
      <div class="flex">
        <div class="text-1xl tracking-wider">@Thawani node docs</div>
      </div>
      <div class="text-gray-500 mt-1 text-xs">
        This Documentation is to make the development process easier for you
      </div>

      <!-- here the seession documentation -->
      <div class="flex-1 lg:flex lg:space-x-8">
        <div class="hidden lg:block lg:w-64">
          <div class="fixed mt-12 z-10">
            <div v-for="doc in docs" :key="doc.title" class="">
              <span class="p-2 cursor-pointer text-green-500 hover:text-green-700 " v-scroll-to="`#${toLower(doc.target)}`">{{doc.slug}}</span>

            </div>
              <span class="p-2 cursor-pointer text-green-500 hover:text-green-700 "> <nuxt-link to="old-version" class="underline"> version < 1.1.0</nuxt-link> </span>
          </div>
        </div>
        <div class="flex-grow">
          <div v-for="doc in docs" :key="doc.title">
            <nuxt-content
              :document="doc"
              class="prose p-2 max-w-none w-full my-1 lg:my-8 lg:mt-20 lg:prose-sm lg:mx-auto lg:p-0"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="text-1xl tracking-wider py-4">Crafted with 🔨 Nuxtjs & tailwindcss </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const docs = await $content("docs").sortBy("order", "asc").fetch();
    return { docs };
  },

  methods: {
    toLower(str) { 
      return str.toLowerCase()
    }
  }
};
</script>
