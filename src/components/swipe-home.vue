<template>
    <mt-swipe :auto="4000" :show-indicators="false">
      <mt-swipe-item class="slide1">
        <img v-bind:src="swipe1">
      </mt-swipe-item>
      <mt-swipe-item class="slide2">
        <img v-bind:src="swipe2">
      </mt-swipe-item>
      <mt-swipe-item class="slide3">
        <img v-bind:src="swipe3">
      </mt-swipe-item>
    </mt-swipe> 
</template>

<script>
import Vue from 'vue'
import {Swipe, SwipeItem} from 'mint-ui'

Vue.component(Swipe.name, Swipe)
Vue.component(SwipeItem.name, SwipeItem)

export default {
  name: 'swipe',
  data () {
    return {
      msg: 'bbbb',
      swipe1: 'http://gc-img.oss-cn-qingdao.aliyuncs.com/banner2-1482289573.jpg',
      swipe2: 'http://gc-img.oss-cn-qingdao.aliyuncs.com/banner640_206-1482131336.png',
      swipe3: 'http://gc-img.oss-cn-qingdao.aliyuncs.com/640jzsc-1481768056.jpg',
    }
  }
}
</script>

<style scoped>
.mint-swipe {
  height: 120px;
  color: #fff;
  font-size: 30px;
  text-align: center;
  margin-bottom: 0px;
}
.mint-swipe img {
  width: 100%;
  height: 100%;
}
.mint-swipe-item {
  line-height: 120px;
}

.slide1 {
  /*background: url('http://gc-img.oss-cn-qingdao.aliyuncs.com/banner2-1482289573.jpg');*/
  /*background-color: #0089dc;*/
  color: #fff;
}

.slide2 {
  /*background-color: #ffd705;*/
  /*background: url('http://gc-img.oss-cn-qingdao.aliyuncs.com/banner640_206-1482131336.png');*/
  color: #fff;
}

.slide3 {
  /*background-color: #ff2d4b;*/
  /*background: url('http://gc-img.oss-cn-qingdao.aliyuncs.com/banner2-1482289573.jpg');*/
  color: #fff;
}

</style>
<style>
.mint-swipe .mint-swipe-indicators{
  bottom:0;
}
</style>
