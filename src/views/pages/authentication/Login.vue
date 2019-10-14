<template>
  <vue-scroll class="login-page align-vertical">
    <div class="form-wrapper align-vertical-middle">
      <div class="form-box card-base card-shadow--extraLarge">
        <img class="image-logo" src="@/assets/images/logo.png" alt="Standard Bank" />

        <div class="page-header platform-title">
          <h1>Cards Platform</h1>
        </div>
        <float-label class="styled">
          <input type="email" placeholder="A - Number" />
        </float-label>
        <float-label class="styled">
          <input type="password" placeholder="Password" />
        </float-label>
        <div class="flex">
          <div class="box grow">
            <el-checkbox>Remember Me</el-checkbox>
          </div>
        </div>

        <div class="flex text-center center pt-30 pb-10">
          <el-button plain size="small" @click="login" class="login-btn tada animated">LOGIN</el-button>
        </div>
      </div>
    </div>
  </vue-scroll>
</template>

<script>
export default {
  name: "Login",
  data() {
    return {
      form: {
        email: "",
        password: ""
      }
    };
  },
  methods: {
    login() {
      this.$store.commit("setLogin");
      this.$router.push("dashboard");
    }
  }
};
</script>

<style lang="scss">
@import "../../../assets/scss/_variables";

.login-page {
  background: $text-color;
  margin-left: -30px;
  margin-right: -30px;

  .form-wrapper {
    width: 100%;
  }

  .form-box {
    width: 100%;
    max-width: 400px;
    padding: 30px;
    box-sizing: border-box;
    margin: 20px auto;

    a {
      font-size: 14px;
      color: $text-color-accent;
      text-decoration: none;
      font-weight: 500;
    }

    .image-logo {
      width: 80px;
      margin: 0px auto;
      margin-bottom: 30px;
      display: block;
      margin-bottom: 0;
    }

    .login-btn {
      width: 70%;
      margin-left: 15%;
      margin-right: 15%;
    }

    .platform-title {
      text-align: center;
      vertical-align: middle;
      line-height: 90px;
    }

    .vfl-has-label.styled {
      max-width: 400px;
      margin-left: 15%;
      margin-right: 15%;
      width: 70%;
    }

    .el-checkbox__label {
      margin-left: 20%;
      margin-right: 20%;
    }

    .flex > .box.grow {
      margin-left: 15%;
      margin-right: 15%;
    }
  }
}

@media (max-width: 768px) {
  .layout-container .container .view.login-page {
    margin-left: -5px;
    margin-right: -5px;
    max-width: calc(100% + 10px);
  }
}
</style>
