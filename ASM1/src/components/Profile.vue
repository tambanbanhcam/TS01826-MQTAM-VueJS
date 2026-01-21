<template>
  <div class="row justify-content-center">
    <div class="col-md-8">
      <h2 class="mb-4">Hồ sơ cá nhân</h2>
      <div class="card shadow">
        <div class="card-body">
          <div class="text-center mb-4">
            <img src="/src/assets/images/image.jpg" alt="Avatar" class="rounded-circle" width="120" height="120">
            <h4 class="mt-3">{{ user.name }}</h4>
            <p class="text-muted">{{ user.email }}</p>
          </div>
          <hr>
          <h5>Chỉnh sửa thông tin</h5>
          <form>
            <div class="mb-3">
              <label class="form-label">Họ và tên</label>
              <input type="text" class="form-control" v-model="user.name">
            </div>
            <div class="mb-3">
              <label class="form-label">Email</label>
              <input type="email" class="form-control" v-model="user.email">
            </div>
            <div class="mb-3">
              <label class="form-label">Mật khẩu mới (để trống nếu không đổi)</label>
              <input type="password" class="form-control">
            </div>
            <div class="d-grid">
              <button type="submit" class="btn btn-primary">Lưu thay đổi</button>
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
      user: {
        name: 'Mai Quốc Tam',
        email: 'tam@example.com'
      }
    }
  }
}
</script>