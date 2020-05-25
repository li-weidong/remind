<template>
  <div class="login">
    <div class="left"></div>
    <div class="right">
      <div class="right-center">
        <el-tabs type="border-card" :stretch="true">
          <el-tab-pane label="登陆">
            <el-form
              :model="this.login.ruleForm"
              :rules="this.login.rules"
              ref="ruleForm"
          
              class="demo-ruleForm"
              style="margin:0 20px"
            >
              <el-form-item>
                <el-input
                  v-model="login.ruleForm.name"
                  placeholder="请输入账号"
                  prefix-icon="el-icon-user"
                ></el-input>
              </el-form-item>
              <el-form-item>
                <el-input
                  v-model="login.ruleForm.password"
                  placeholder="请输入密码"
                  prefix-icon="el-icon-lock"
                ></el-input>
              </el-form-item>
              <el-form-item>
                <el-button type="primary" style="width:100%" @click="hanleLogin">登陆</el-button>
              </el-form-item>
            </el-form>
          </el-tab-pane>
          <el-tab-pane label="注册">
            <el-form
              :model="this.login.ruleForm"
              :rules="this.login.rules"
              ref="ruleForm"
          
              class="demo-ruleForm"
              style="margin:0 20px"
            >
              <el-form-item>
                <el-input
                  v-model="login.ruleForm.name"
                  placeholder="请输入账号"
                  prefix-icon="el-icon-user"
                ></el-input>
              </el-form-item>
              <el-form-item>
                <el-input
                  v-model="login.ruleForm.password"
                  placeholder="请输入密码"
                  prefix-icon="el-icon-lock"
                ></el-input>
              </el-form-item>
              <el-form-item>
                <el-button type="primary" style="width:100%">注册</el-button>
              </el-form-item>
            </el-form>
          </el-tab-pane>
        </el-tabs>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "login",
  components: {},
  data() {
    return {
      login: {
        ruleForm: {
          name: "",
          password: ""
        },
        rules: {
          name: [{ required: true, message: "请输入用户名", trigger: "blur" }],
          password: [{ required: true, message: "请输入密码", trigger: "blur" }]
        }
      }
    };
  },
  methods: {
    hanleLogin(){
      this.$router.push({ path:'/'})
    },
  },
  mounted() {}
};
</script>
<style lang="scss" scoped>
.login {
  width: 100%;
  .left {
    float: left;
    width: 50%;
    height: 100vh;
    // background: red;
  }
  .right {
    float: right;
    width: 50%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    // background: blue;
    .right-center {
      width: 500px;
      height: 200px;
      background: burlywood;
    }
  }
}
</style>