<template>
  <div class="container">
    <el-carousel>
      <el-carousel-item v-for="(item,index) in banners"
                        :key="index">
        <div class="banner-image"
             :style="`background:url(${item.url}) center center no-repeat;background-size:contain contain;`"></div>
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  data () {
    return {
      banners: [
        {
          url: "http://157.122.54.189:9095/assets/images/th03.jfif",
        },
        {
          url: "http://157.122.54.189:9095/assets/images/th04.jfif",
        }
      ]
    }
  }
}
</script>
<style lang="less" scoped>
.container {
  min-width: 1000px;
  margin: 0 auto;
  position: relative;

  /deep/ .el-carousel__container {
    height: 700px;
  }

  .banner-image {
    width: 100%;
    height: 100%;
  }
}
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>