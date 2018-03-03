<template>
  <div class="flex flex-col items-center w-3/4 my-10">
    <div class="mb-10 text-center flex flex-col items-center">
      <h1
        class="font-bold text-4xl w-2/3 mb-6"
        v-text="post.title"/>
      <div class="flex text-xs justify-around w-1/2 text-grey mb-10">
        <div>Destination Eurodive</div>
        &#8226;
        <div>Added by John Williams Doe</div>
        &#8226;
        <div>January 01, 2018</div>
      </div>
      <img
        src="https://source.unsplash.com/random/?nature,water"
        :alt="post.title"
        class="w-full"
        height="100%"
        width="100%">
    </div>
    <div
      class="w-3/4 leading-loose text-justify text-sm mb-10"
      v-text="post.body"/>
    <div class="text-center">
      <nuxt-link
        :to="{ name: 'posts-id', params: { id: post.id }}"
        class="no-underline tracking-wide text-black uppercase px-8 py-3 border border-grey rounded-full text-xs font-medium hover:bg-grey">Read More</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Post",
  props: {
    post: { type: Object, required: true }
  }
};
</script>
