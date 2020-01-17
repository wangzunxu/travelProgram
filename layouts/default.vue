<template>
  <div class="tonglan">
    <div class="main">
      <Header></Header>
    </div>
    <nuxt />

    <Footer></Footer>

  </div>
</template>

<style>
.ditong {
  width: 100%;
  background-color: #333333;
}
* {
  margin: 0;
  padding: 0;
}
ul,
li,
ol {
  list-style: none;
}
a {
  text-decoration: none;
  color: inherit;
}
em,
i {
  font-style: normal;
}
</style>

<script>
import Header from '@/components/header'
import Footer from '@/components/footer'
export default {
  components: {
    Header, Footer
  }
}
</script>

<style lang="less" scoped>
.main {
  width: 1000px;
  margin: 0 auto;
}
</style>
