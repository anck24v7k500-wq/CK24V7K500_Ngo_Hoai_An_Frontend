<template>
  <div class="page mt-5">
    <div class="card" style="max-width: 400px; margin: auto; padding: 20px">
      <h3 class="text-center">Đăng Nhập</h3>
      <form @submit.prevent="handleLogin">
        <div class="form-group">
          <label>Tên đăng nhập</label>
          <input
            type="text"
            class="form-control"
            v-model="username"
            placeholder="Nhập: admin"
            required
          />
        </div>
        <div class="form-group">
          <label>Mật khẩu</label>
          <input
            type="password"
            class="form-control"
            v-model="password"
            placeholder="Nhập: 123456"
            required
          />
        </div>
        <button type="submit" class="btn btn-primary btn-block mt-3">
          Đăng nhập
        </button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    handleLogin() {
      // Làm giả lập tài khoản admin cho thầy coi
      if (this.username === "admin" && this.password === "123456") {
        alert("Đăng nhập thành công!");
        this.$router.push({ name: "contactbook" }); // Chuyển về trang chủ
      } else {
        alert("Sai tài khoản hoặc mật khẩu!");
      }
    },
  },
};
</script>
