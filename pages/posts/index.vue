<template>
  <div>
    <h3>Posts</h3>
    <pre>
      <code>
        {{ posts }}
      </code>
    </pre>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data() {
    return {
      posts: []
    }
  },
  async asyncData() {
    const { data } = await axios.get('https://jsonplaceholder.typicode.com/posts')

    return { posts: data }
  },
  mounted() {
    this.posts
  }
}
</script>
