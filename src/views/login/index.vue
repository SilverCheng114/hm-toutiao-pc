<template>
  <div class='container-login'>
      <el-card class="my-card">
          <!-- logo图片 -->
          <img src="../../assets/logo_index.png" />
          <!-- 表单 -->
          <el-form :model="loginForm">
              <el-form-item>
                  <el-input v-model="loginForm.mobile" placeholder="请输入手机号"></el-input>
              </el-form-item>
              <el-form-item>
                  <el-input v-model="loginForm.code" placeholder="请输入验证码" style="width:235px;margin-right:10px"></el-input>
                  <el-button>发送验证码</el-button>
              </el-form-item>
              <el-form-item>
                  <el-checkbox :value="true">我已阅读并同意用户协议和隐私条款</el-checkbox>
              </el-form-item>
              <el-form-item>
                  <el-button type="primary" style="width:100%">登录</el-button>
              </el-form-item>
          </el-form>
      </el-card>
  </div>
</template>

<script>
export default {
  data () {
    return {
      loginForm: {
        mobile: '',
        code: ''
      }
    }
  }
}
</script>

<style lang="less" scoped>
    .container-login{
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height:100%;
        background: url(../../assets/login_bg.jpg) no-repeat center / cover;
        .my-card{
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%,-50%);
            width: 400px;
            height: 350px;
            img{
                display: block;
                width: 200px;
                margin: 0 auto 20px;
            }
        }
    }
</style>
