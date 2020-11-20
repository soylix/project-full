<template>
  <div>
    <el-form class="login-form">
      <el-form-item props="email">
        <span><i class="el-icon-mobile"></i></span>
        <el-input placeholder="邮箱"></el-input>
      </el-form-item>
      <el-form-item props="passwd">
        <span><i class="el-icon-lock"></i></span>
        <el-input placeholder="密码"></el-input>
      </el-form-item>
      <el-form-item props="captcha">
        <el-input placeholder="验证码"></el-input>
        <img @click="updataCaptcha" :src="captchaUrl" alt="">
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  layout: 'login',
  props: {

  },
  data() {
    return {
      rules: [

      ],
      captchaUrl: '/api/captcha?_t=' + new Date().getTime(),
    };
  },
  computed: {

  },
  created() {

  },
  mounted() {

  },
  watch: {

  },
  methods: {
    updataCaptcha() {
      this.captchaUrl = 'api/captcha?_t=' + new Date().getTime();
    }
  },
  components: {

  },
};
</script>

<style lang="stylus">
.login-form
  width 800px
  margin 50px auto
</style>
