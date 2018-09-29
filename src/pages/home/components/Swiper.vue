<template>
<div class="wrapper">
 <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data (){
      return{
          swiperOption: {
              pagination:'.swiper-pagination',
              loop:true
          },
          swiperList:[{
              id:'0001',
              imgUrl:'http://img1.qunarzz.com/piao/fusion/1809/2d/0d7dc3400a50b502.jpg_750x200_4ca95dd4.jpg'
          },{
              id:'0002',
              imgUrl:'http://img1.qunarzz.com/piao/fusion/1807/78/0a6355bcbbf89502.jpg_750x200_fc738633.jpg'
          }]
      }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background :#fff
.wrapper
  overflow :hidden
  width :100%
  height :0
  padding-bottom :31.25%
  background ：#eee
  .swiper-img
    width:100%
</style>