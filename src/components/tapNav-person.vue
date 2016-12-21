<template>  
<div>
  <mt-navbar v-model="selected">
    <mt-tab-item id="1">最近在玩</mt-tab-item>
    <mt-tab-item id="2">推送设置</mt-tab-item>
  </mt-navbar>
  <!-- tab-container -->
  <mt-tab-container v-model="selected">
    <mt-tab-container-item id="1">
      <tapNavContent1 :selected="selected=='1'"></tapNavContent1>
    </mt-tab-container-item>
    <mt-tab-container-item id="2">
      <tapNavContent2 :selected="selected=='2'"></tapNavContent2>
    </mt-tab-container-item>
  </mt-tab-container>
</div> 
</template>

<script>
import Vue from 'vue'
import { Navbar, TabItem } from 'mint-ui'
import { TabContainer, TabContainerItem } from 'mint-ui'
import tapNavContent1 from './tapNavContent1-person'
import tapNavContent2 from './tapNavContent2-person'

Vue.component(Navbar.name, Navbar);
Vue.component(TabItem.name, TabItem);
Vue.component(TabContainer.name, TabContainer);
Vue.component(TabContainerItem.name, TabContainerItem);

export default {
  name: 'swipe',
  data () {
    return {
      selected: '1'
    }
  },
  mounted(){
    // var index = this.$store.getters.getIndex;
    // if(index){
    //   this.selected = index;
    // }
  },
  components: { 
    tapNavContent1,
    tapNavContent2
  }
}
</script>

<style scoped>
.mint-navbar .mint-tab-item.is-selected{
  margin-bottom: 0;
}
</style>
<style>

</style>
