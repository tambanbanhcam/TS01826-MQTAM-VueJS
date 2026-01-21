<template>
  <div>
    <button class="btn btn-secondary mb-4" @click="$parent.currentPage = 'home'">← Quay lại</button>
    
    <div class="card shadow">
      <img src="/src/assets/images/image.jpg" class="card-img-top" alt="Post image" style="height: 400px; object-fit: cover;">
      <div class="card-body">
        <h2 class="card-title">Tiêu đề bài viết mẫu</h2>
        <p class="text-muted">Đăng bởi: Tam | 21/01/2026</p>
        <p class="card-text">
          Đây là nội dung chi tiết của bài viết. Bạn có thể viết dài bao nhiêu tùy thích. 
          Nội dung này được hiển thị đầy đủ khi xem chi tiết.
        </p>
      </div>
    </div>

    <h4 class="mt-5 mb-3">Bình luận</h4>
    <div class="accordion" id="commentAccordion">
      <div class="accordion-item">
        <h2 class="accordion-header">
          <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#addComment">
            Thêm bình luận mới
          </button>
        </h2>
        <div id="addComment" class="accordion-collapse collapse show">
          <div class="accordion-body">
            <textarea class="form-control mb-3" rows="3" placeholder="Viết bình luận..."></textarea>
            <button class="btn btn-primary">Gửi bình luận</button>
          </div>
        </div>
      </div>
    </div>

    <div class="mt-4">
      <div class="card mb-3" v-for="comment in comments" :key="comment.id">
        <div class="card-body">
          <strong>{{ comment.user }}</strong> <small class="text-muted">{{ comment.time }}</small>
          <p class="mb-0 mt-2">{{ comment.text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      comments: [
        { id: 1, user: 'Lan', time: '10:15', text: 'Bài viết rất hay, cảm ơn bạn!' },
        { id: 2, user: 'Minh', time: '09:45', text: 'Mình cũng đang học Vue, rất hữu ích.' }
      ]
    }
  }
}
</script>