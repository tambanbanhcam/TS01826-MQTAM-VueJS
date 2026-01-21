<template>
  <div>
    <h2 class="mb-4">Bài viết của tôi</h2>
    <div class="table-responsive">
      <table class="table table-striped table-hover shadow-sm">
        <thead class="table-dark">
          <tr>
            <th>Tiêu đề</th>
            <th>Ngày đăng</th>
            <th>Lượt xem</th>
            <th>Hành động</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="post in myPosts" :key="post.id">
            <td>{{ post.title }}</td>
            <td>{{ post.date }}</td>
            <td>{{ post.views }}</td>
            <td>
              <button class="btn btn-sm btn-warning me-2">Sửa</button>
              <button class="btn btn-sm btn-danger">Xóa</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      myPosts: [
        { id: 1, title: 'Khám phá Vue 3', date: '21/01/2026', views: 245 },
        { id: 2, title: 'Bootstrap 5 Tips', date: '20/01/2026', views: 189 }
      ]
    }
  }
}
</script>