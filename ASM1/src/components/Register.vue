<template>
  <div class="row justify-content-center">
    <div class="col-md-6 col-lg-5">
      <div class="card shadow">
        <div class="card-body p-4">
          <h3 class="card-title text-center mb-4">Đăng ký tài khoản</h3>
          <form>
            <div class="mb-3">
              <label class="form-label">Họ và tên</label>
              <input type="text" class="form-control" v-model="name">
            </div>
            <div class="mb-3">
              <label class="form-label">Email</label>
              <input type="email" class="form-control" v-model="email">
            </div>
            <div class="mb-3">
              <label class="form-label">Mật khẩu</label>
              <input type="password" class="form-control" v-model="password">
            </div>
            <div class="mb-3">
              <label class="form-label">Xác nhận mật khẩu</label>
              <input type="password" class="form-control" v-model="confirmPassword">
            </div>
            <div class="d-grid">
              <button type="submit" class="btn btn-success">Đăng ký</button>
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
      name: '',
      email: '',
      password: '',
      confirmPassword: ''
    }
  }
}
</script>