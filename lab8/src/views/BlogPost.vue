<template>
  <div>
    <h2>{{ post.title }}</h2>
    <p>{{ post.content }}</p>
    <router-link to="/blog">Back to Blog List</router-link>
  </div>
</template>

<script>
export default {
  name: 'BlogPostView',
  data() {
    return {
      posts: [
        { id: 1, title: 'hello', content: 'Em ben 10 gió' },
        { id: 2, title: 'tachahao', content: '67' },
        { id: 3, title: 'xinchao', content: '36' }
      ],
      post: {}
    }
  },
  created() {
    const postId = parseInt(this.$route.params.id)
    this.post = this.posts.find(p => p.id === postId) || {}
  }
}
</script>