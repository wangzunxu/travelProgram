<template>
  <div class="container">
    <el-form :model="form"
             ref="form"
             :rules="rules"
             class="form">
      <el-form-item>
        <el-row type="flex"
                justify="space-around"
                class="select">
          <span @click="current=1"
                :class="{active:current===1}">登录</span>
          <span @click="current=2"
                :class="{active:current===2}">注册</span>
        </el-row>
      </el-form-item>

      <el-form-item class="form-item">
        <el-input v-model="user.username"
                  placeholder="用户名/手机"
                  v-if="current===1">
        </el-input>
        <el-input v-model="rigUser.RigUsername"
                  placeholder="用户名/手机"
                  v-if="current===2">
        </el-input>
      </el-form-item>

      <el-form-item class="form-item">
        <el-input placeholder="密码"
                  type="password"
                  v-if="current===1"
                  v-model="user.password">
        </el-input>
        <el-row v-if="current===2"
                type="flex">
          <el-input placeholder="密码"
                    type="password"
                    class="yanz">
          </el-input>
          <el-button type="primary">发送验证码</el-button>
        </el-row>
      </el-form-item>
      <el-form-item class="form-item"
                    v-if="current===2">
        <el-input placeholder="你的名字">
        </el-input>
      </el-form-item>
      <el-form-item class="form-item"
                    v-if="current===2">
        <el-input placeholder="密码">
        </el-input>
      </el-form-item>
      <el-form-item class="form-item"
                    v-if="current===2">
        <el-input placeholder="确认密码">
        </el-input>
      </el-form-item>
      <p class="form-text">
        <nuxt-link to="#">忘记密码</nuxt-link>
      </p>

      <el-button class="submit"
                 type="primary"
                 @click="handleLoginSubmit"
                 v-if="current===1">
        登录
      </el-button>
      <el-button class="submit"
                 type="primary"
                 @click="handleLoginSubmit"
                 v-if="current===2">
        注册
      </el-button>
    </el-form>
  </div>
</template>

<script>
export default {
  data () {
    return {
      rigUser: {
        rigUsername: '',
        rigPassword: ''
      },
      user: {
        username: '',
        password: ''
      },
      current: 1,
      // 表单数据
      form: {},
      // 表单规则
      rules: {},
    }
  },
  methods: {
    // 提交登录
    handleLoginSubmit () {
      console.log(this.form)
    }
  }
}
</script>

<style lang="less" scoped >
.form {
  padding: 25px;
}

.form-item {
  margin-bottom: 20px;
}

.form-text {
  font-size: 12px;
  color: #409eff;
  text-align: right;
  line-height: 1;
}

.submit {
  width: 100%;
  margin-top: 10px;
}
.select {
  background-color: #eee;
  font-size: 16px;
  span {
    display: inline-block;
    width: 50%;
    text-align: center;
  }
}
.active {
  color: orange;
  border-top: 2px solid orange;
  background-color: #fff;
  font-weight: 700;
}
.yanz {
  flex: 1;
}
</style>