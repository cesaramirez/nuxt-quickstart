<template>
  <div>
    <h3 class="text-red">Posts</h3>
    <div class="container mx-auto flex flex-col items-center">
      <post/>
    </div>
  </div>
</template>

<script>
import Post from '@/components/post'
export default {
  name: 'Posts',
  components: {
    Post
  },
  data() {
    return {
      posts: []
    };
  },
  async asyncData({ app }) {
    const data = await app.$axios.$get(
      "https://jsonplaceholder.typicode.com/posts"
    );
    return { posts: data };
  }
};
</script>
