<template>
  <div>
    <h3 class="text-red">Posts</h3>
    <div class="flex flex-col items-center">
      <post v-for="post in posts" :key="post.id" :post="post" class="mb-10"/>
    </div>
  </div>
</template>

<script>
import Post from "@/components/post";
export default {
  name: "Posts",
  components: {
    Post
  },
  head: {
    title: "Posts"
  },
  data() {
    return {
      posts: []
    };
  },
  async asyncData({ app, error }) {
    try {
      const data = await app.$axios.$get(
        "https://jsonplaceholder.typicode.com/posts"
      );
      return { posts: data };
    } catch (e) {
      error({ statusCode: e.response.status });
    }
  }
};
</script>
