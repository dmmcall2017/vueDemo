<template>
  <div class="home">
      <div class="top">
          <div class="header">
              <el-row :gutter="20">
                <el-col :span="4"><div class="grid-content bg-purple"><i class="iconfont icon-liebiao"></i></div></el-col>
                <el-col :span="16">
                    <div class="grid-content bg-purple">
                        <span class="iconfont icon-search"></span><input placeholder="输入……" class="searchContext"/>
                    </div>
                </el-col>
                <el-col :span="4"><div class="grid-content bg-purple" @click="login">登录</div></el-col>
              </el-row>
          </div>
          <div class="banner">
              <div class="swiper-container">
                <div class="swiper-wrapper">
                    <div class="swiper-slide"><img src="@/assets/home/1.jpg"/></div>
                    <div class="swiper-slide"><img src="@/assets/home/2.jpg"/></div>
                    <div class="swiper-slide"><img src="@/assets/home/1.jpg"/></div>
                    <div class="swiper-slide"><img src="@/assets/home/2.jpg"/></div>
                </div>
              </div>
          </div>
      </div>
      <div class="content"></div>
      <div class="footer">
          
      </div>
  </div>
</template>

<script>
import Swiper from 'swiper'
import 'swiper/dist/css/swiper.min.css'
export default {
  name: 'home',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  mounted(){
    new Swiper ('.swiper-container', {
        loop: true
    })        
  },
  methods:{
      login(){
          this.$router.replace('/login')
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .swiper-slide>img{
        width:100%;
    }
    .header{
        position:absolute;
        z-index:100;
        width: 100%;
        box-sizing: border-box;
        padding: 5px 10px;
        color:#fff;
        height:40px;
        line-height:40px;
    }
    .searchContext{
        border-radius: 15px;
        border: 0;
        box-sizing: border-box;
        padding-left: 5px;
        height:30px;
        line-height:30px;
        width:100%;
    }
    .icon-search{
        position: absolute;
        right: 10px;
        color: #333;
    }
    .grid-content.bg-purple{
        position:relative;
    }
</style>
