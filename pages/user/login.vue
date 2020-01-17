<template>
  <div class="container"
       style="background:url('http://157.122.54.189:9095/assets/images/th03.jfif')">
    <LoginForm class="lo"></LoginForm>
  </div>
</template>

<script>
import LoginForm from '@/components/user/loginForm'
export default {
  components: {
    LoginForm
  }
}
</script>

<style lang="less" scoped>
.container {
  width: 100%;
  height: 700px;
  .lo {
    position: absolute;
    left: 50%;
    top: 30%;
    transform: translateX(-50%);
    width: 400px;
    height: 243px;
  }
}
</style>