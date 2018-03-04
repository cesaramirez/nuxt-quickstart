<template>
  <div class="text-center">
    <h3 class="text-4xl text-white mb-10">Home</h3>
    <nuxt-link
      :to="{ name: 'posts' }"
      class="text-black bg-white px-8 py-4 border rounded-full no-underline uppercase font-bold hover:bg-grey-light">Go to Posts</nuxt-link>
  </div>
</template>

<script>

export default {
  layout: 'home'
}
</script>
