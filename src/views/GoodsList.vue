<template>
 <div>
   这是商品列表
   <span>{{$route.params.goodsId}}</span><br>
   <span>{{$route.params.name}}</span>
   <router-link to="/goods/title">显示商品标题</router-link>
   <router-link to="/goods/img">显示商品图片</router-link>
   <div>
     <router-view></router-view>
   </div>
   <router-link v-bind:to="{name:'cart'}">跳转到购物车页面</router-link>
 </div>
</template>

<script>
  export default{
    data(){
      return {
        msg: "是谁把你带到我身边"
      }
    },
    methods:{
        jump(){
          this.$router.push({path:'/cart?goodsId=123'});
        }
    }
  }
</script>
