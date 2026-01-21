<template>
  <div class="row justify-content-center">
    <div class="col-md-6 col-lg-5">
      <div class="card shadow">
        <div class="card-body p-4">
          <h3 class="card-title text-center mb-4">Đăng nhập</h3>
          <form>
            <div class="mb-3">
              <label class="form-label">Email</label>
              <input type="email" class="form-control" v-model="email" placeholder="example@email.com">
            </div>
            <div class="mb-3">
              <label class="form-label">Mật khẩu</label>
              <input type="password" class="form-control" v-model="password">
            </div>
            <div class="d-grid">
              <button type="submit" class="btn btn-primary">Đăng nhập</button>
            </div>
          </form>
          <div class="text-center mt-3">
            <small>Chưa có tài khoản? 
              <a href="#" class="text-primary" @click.prevent="$parent.currentPage = 'register'">Đăng ký</a>
            </small>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: ''
    }
  }
}
</script>