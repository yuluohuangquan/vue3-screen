<template>
  <div class="login">
    <el-card shadow="hover" class="login-content">
        <el-form ref="formRef" :model="loginForm" label-width="80px">
          <el-form-item label="名称">
            <el-input v-model="loginForm.name"></el-input>
          </el-form-item>
          <el-form-item label="密码">
            <el-input
              v-model="loginForm.password"
              type="password"
              show-password
            />
          </el-form-item>
        </el-form>
        <el-button type="primary" @click="submit()">登录</el-button>
    </el-card>
  </div>
</template>

<script lang="ts">
import { reactive } from "vue";
import { useRouter } from "vue-router";
export default {
  name: "Login",
  setup() {
    const loginForm = reactive({
      name: "",
      password: "",
    });

    const router = useRouter();

    const submit = () => {
      console.log(loginForm);
      router.push("/");
    };

    return { loginForm, submit };
  },
};
</script>

<style lang="less" scoped>
.login {
  width: 100%;
  height: 100%;
  background-image: url("../assets/login_bg.png");
  background-size: 100%;
  .login-content {
    position: absolute;
    width: 320px;
    height: 140px;
    top: 200px;
    margin: 0 auto;
    text-align: center;
    padding: 24px;
    left: 50%;
    margin-left: -160px;
  }
}
</style>