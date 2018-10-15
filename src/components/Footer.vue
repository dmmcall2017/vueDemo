<template>
  <div class="footer" id="footer">
     <ul>
         <li v-for="(item,index) in tabs" :key="index" @click="changeTab(index)" :class="index==currentIndex?current:''">
             <i :class="item.icon"></i><br>
             <span>{{ item.title }}</span>
         </li>
     </ul>
  </div>
</template>

<script>
export default {
  name: 'footer',
  data () {
    return {
      tabs:[
          {title:'首页',icon:'iconfont icon-shouye',path:'/'},
          {title:'分类',icon:'iconfont icon-fenlei',path:''},
          {title:'拼购',icon:'iconfont icon-pintuangou',path:''},
          {title:'购物车',icon:'iconfont icon-gouwuche1',path:''},
          {title:'未登录',icon:'iconfont icon-tubiao211',path:''}
      ],
      currentIndex:'0',
      current:'current'
    }
  },
  methods:{
      changeTab(index){
          this.currentIndex = index;
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .footer{
        width:100%;
        position:fixed;
        bottom:0;
        box-sizing: border-box;
        padding: 10px 0;
        box-shadow: 0 -1px 10px rgba(0,0,0,.5);
        bottom: 0;
        background: #fff;
    }
    .footer ul>li{
        float: left;
        width:20%;
        text-align: center;
    }
    .footer ul>li>i{
        font-size:18px;
    }
    .footer ul>.current{
        color:#f00;
    }
</style>
