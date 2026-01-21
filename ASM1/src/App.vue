<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <a class="navbar-brand" href="#" @click.prevent="currentPage = 'home'">Blog App</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <a class="nav-link" href="#" @click.prevent="currentPage = 'home'">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#" @click.prevent="currentPage = 'create-post'">Create Post</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#" @click.prevent="currentPage = 'my-posts'">My Posts</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#" @click.prevent="currentPage = 'profile'">Profile</a>
          </li>
        </ul>
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" href="#" @click.prevent="currentPage = 'login'">Login</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#" @click.prevent="currentPage = 'register'">Register</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <div class="container mt-4">
    <!-- Conditional rendering các trang -->
    <div v-if="currentPage === 'home'">
      <Home />
    </div>
    <div v-else-if="currentPage === 'login'">
      <Login />
    </div>
    <div v-else-if="currentPage === 'register'">
      <Register />
    </div>
    <div v-else-if="currentPage === 'profile'">
      <Profile />
    </div>
    <div v-else-if="currentPage === 'create-post'">
      <CreatePost />
    </div>
    <div v-else-if="currentPage === 'my-posts'">
      <MyPosts />
    </div>
    <div v-else-if="currentPage === 'post-detail'">
      <PostDetail />
    </div>
    <div v-else>
      <h1>Trang không tồn tại</h1>
    </div>
  </div>
</template>

<script>
import Home from './components/Home.vue'
import Login from './components/Login.vue'
import Register from './components/Register.vue'
import Profile from './components/Profile.vue'
import CreatePost from './components/CreatePost.vue'
import MyPosts from './components/MyPosts.vue'
import PostDetail from './components/PostDetail.vue'

export default {
  components: {
    Home,
    Login,
    Register,
    Profile,
    CreatePost,
    MyPosts,
    PostDetail
  },
data() {
  return {
    currentPage: 'home',
    selectedPostId: null
  }
}
}

</script>

<style>
/* Optional: style active link */
.nav-link.active {
  color: #0d6efd !important;
  font-weight: bold;
}
</style>