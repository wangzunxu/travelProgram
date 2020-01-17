<template>
  <div class="header">
    <el-row type="flex"
            justify="space-around">
      <div class="logo">
        <img src="@/static/logo.jpg"
             alt="">
      </div>
      <el-row class="nav"
              type="flex">
        <nuxt-link to="/">首页</nuxt-link>
        <nuxt-link to="/air">国内机票</nuxt-link>
        <nuxt-link to="/hotel">酒店</nuxt-link>
        <nuxt-link to="/post">旅游攻略</nuxt-link>
      </el-row>
      <div class="login">
        <nuxt-link to="/user/login">登录/注册</nuxt-link>
      </div>
    </el-row>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped lang="less">
.header {
  height: 60px;
  line-height: 60px;
}
.logo {
  width: 156px;
  padding: 8px 0 0;
  img {
    display: block;
    width: 100%;
  }
}
/deep/.nav {
  flex: 1;
  font-size: 16px;
  > a {
    display: block;
    height: 60px;
    box-sizing: border-box;
    padding: 0 20px;
    &:hover {
      border-bottom: #409eff solid 4px;
      color: #409eff;
    }
  }
}
.login {
  cursor: pointer;
}
.nuxt-link-exact-active {
  background-color: #409eff;
  color: #fff;
}
</style>
