<template>
  <div class="flex flex-col items-center my-10">
    <div class="mb-10 text-center flex flex-col items-center">
      <h1 class="font-bold text-4xl w-2/3 mb-6" v-text="post.title" />
      <div class="flex text-xs justify-around w-1/2 text-grey mb-10">
        <div>Destination Eurodive</div>
        &#8226;
        <div>Added by John Williams Doe</div>
        &#8226;
        <div>January 01, 2018</div>
      </div>
      <img src="https://source.unsplash.com/random/?nature,water" :alt="post.title" height="80%" width="80%">
    </div>
    <div class="w-3/4 leading-loose text-justify text-sm mb-10" v-text="post.body" />
    <div class="bg-grey-lighter p-8 w-2/3 text-center mb-10">
      <p class="font-bold text-xl mb-8">Lorem ipsum dolor sit amet, consectetur adipiscing elit. </p>
      <p>Caption for quote goes here.</p>
    </div>
    <div class="text-center my-10">
      <nuxt-link
        :to="{ name: 'posts' }"
        class="no-underline tracking-wide text-black uppercase px-8 py-3 border border-grey rounded-full text-xs font-medium hover:bg-grey">All Posts</nuxt-link>
    </div>
  </div>
</template>

<script>
  export default {
    name: "PostDetail",
    data() {
      return {
        post: null
      }
    },
    async asyncData({
      params,
      app
    }) {
      const data = await app.$axios.$get(
        `https://jsonplaceholder.typicode.com/posts/${params.id}`
      );
      console.log(data);

      return {
        post: data
      };
    }
  };

</script>
