<template>
  <div class="row justify-content-center">
    <div class="col-lg-8">
      <h2 class="mb-4">Viết bài mới</h2>
      <div class="card shadow">
        <div class="card-body">
          <form>
            <div class="mb-3">
              <label class="form-label">Tiêu đề bài viết</label>
              <input type="text" class="form-control" v-model="title" placeholder="Nhập tiêu đề...">
            </div>
            <div class="mb-3">
              <label class="form-label">Nội dung</label>
              <textarea class="form-control" rows="8" v-model="content" placeholder="Viết nội dung bài viết tại đây..."></textarea>
            </div>
            <div class="mb-3">
              <label class="form-label">Hình ảnh đại diện</label>
              <input type="file" class="form-control">
            </div>
            <div class="d-grid">
              <button type="submit" class="btn btn-success">Đăng bài</button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: '',
      content: ''
    }
  }
}
</script>