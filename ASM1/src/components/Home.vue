<template>
  <div>
    <h2 class="mb-4">Trang chủ - Các bài viết mới</h2>

    <!-- Carousel từ Lab 3 -->
    <div id="blogCarousel" class="carousel slide mb-5" data-bs-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="/src/assets/images/image.jpg" class="d-block w-100 rounded" alt="Banner 1" style="height: 350px; object-fit: cover;">
        </div>
        <div class="carousel-item">
          <img src="/src/assets/vue.svg" class="d-block w-100 rounded" alt="Banner 2" style="height: 350px; object-fit: cover;">
        </div>
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#blogCarousel" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#blogCarousel" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
      </button>
    </div>

    <div class="row g-4">
      <div class="col-md-6 col-lg-4" v-for="post in posts" :key="post.id">
        <div class="card h-100 shadow-sm">
          <img :src="post.image" class="card-img-top" alt="Post" style="height: 180px; object-fit: cover;">
          <div class="card-body">
            <h5 class="card-title">{{ post.title }}</h5>
            <p class="card-text text-muted">{{ post.content.substring(0, 90) }}...</p>
<button class="btn btn-primary btn-sm" @click="$parent.currentPage = 'post-detail'; $parent.selectedPostId = post.id">
  Xem chi tiết
</button>          </div>
        </div>
      </div>
    </div>

    <!-- Pagination từ Lab 3 -->
    <nav aria-label="Page navigation" class="mt-5">
      <ul class="pagination justify-content-center">
        <li class="page-item disabled"><a class="page-link" href="#">Previous</a></li>
        <li class="page-item active"><a class="page-link" href="#">1</a></li>
        <li class="page-item"><a class="page-link" href="#">2</a></li>
        <li class="page-item"><a class="page-link" href="#">Next</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        { id: 1, title: 'Khám phá Vue 3', content: 'Vue 3 mang lại nhiều cải tiến về performance và composition API...', image: '/src/assets/images/image.jpg' },
        { id: 2, title: 'Bootstrap 5 Tips', content: 'Cách sử dụng grid, card, carousel hiệu quả trong dự án...', image: '/src/assets/images/image.jpg' },
        { id: 3, title: 'Học lập trình web', content: 'Hành trình từ HTML/CSS đến Vue + Backend...', image: '/src/assets/images/image.jpg' }
      ]
    }
  }
}
</script>