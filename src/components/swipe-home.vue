<template>
    <mt-swipe :auto="4000" :show-indicators="false">
      <mt-swipe-item class="slide1">1</mt-swipe-item>
      <mt-swipe-item class="slide2">2</mt-swipe-item>
      <mt-swipe-item class="slide3">3</mt-swipe-item>
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
      msg: 'bbbb'
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

.mint-swipe-item {
  line-height: 120px;
}

.slide1 {
  background-color: #0089dc;
  color: #fff;
}

.slide2 {
  background-color: #ffd705;
  color: #fff;
}

.slide3 {
  background-color: #ff2d4b;
  color: #fff;
}

</style>
<style>
.mint-swipe .mint-swipe-indicators{
  bottom:0;
}
</style>
