<template>
  <div class="container mx-auto">
    <h3 class="text-red">Posts</h3>
    <pre>
      <code class="red-text">
        {{ posts }}
      </code>
    </pre>
  </div>
</template>

<script>
export default {
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
