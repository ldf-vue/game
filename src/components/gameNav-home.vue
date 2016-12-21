<template>  
<div id="gameSwipe">
  <mt-navbar v-model="selected">
    <mt-tab-item id="1">咨询</mt-tab-item>
    <mt-tab-item id="2">礼包</mt-tab-item>
  </mt-navbar>
  <!-- tab-container -->
  <mt-tab-container v-model="selected">
    <mt-tab-container-item id="1">
      <gameNews :selected="selected=='1'"></gameNews>
    </mt-tab-container-item>
    <mt-tab-container-item id="2">
      <gameGift :selected="selected=='2'"></gameGift>
    </mt-tab-container-item>
  </mt-tab-container>
</div> 
</template>

<script>
import Vue from 'vue'
import { Navbar, TabItem } from 'mint-ui'
import { TabContainer, TabContainerItem } from 'mint-ui'
import gameNews from './gameContentNwes'
import gameGift from './gameContentGift'

Vue.component(Navbar.name, Navbar);
Vue.component(TabItem.name, TabItem);
Vue.component(TabContainer.name, TabContainer);
Vue.component(TabContainerItem.name, TabContainerItem);

export default {
  name: 'gameSwipe',
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
  watch: {
    selected:function(val, oldVal){
      //将索引变化值记录到store
      //this.$store.state.homeNavIndex.index = this.selected;
      // this.$store.dispatch('setIndex', this.selected);
    }
  },
  components: { 
    gameNews,
    gameGift,
  }
}
</script>

<style scoped>
  .mint-navbar {
    display: inline-block;
    width: 100%;
    height: 35px;
    text-align: center;
  }
  .mint-navbar .mint-tab-item.is-selected{
    margin-bottom: 0;
  }
  .mint-tab-item {
    padding: 9px 35px;
    padding-top: 11px;
    display: inline-block;
    font-size: 1.1em;
    color: #888;
    margin: 0;
    text-align: center;
  }
</style>
<style>


</style>
