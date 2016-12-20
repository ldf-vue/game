<template>  
<ul
  v-infinite-scroll="loadMore"
  infinite-scroll-disabled="scrollDisabled"
  infinite-scroll-distance="30">
  <li v-for="item in list" class="new-service">
    <div>
      <table>
        <tr>
          <td width="5%">
              <img class="game-icon" style="width: 25px; height: 25px;" src="http://h5.hortorgames.com/gc/img/games/jzsc_icon.png" alt="...">
          </td>
          <td width="27%">
              <span>决战沙城</span>
          </td>
          <td width="34%">
              <span>沙城916区</span>
          </td>
          <td width="15%" style="text-align: center;">
              开服<br>2小时
          </td>
          <td width="18%">
              <a class="btn">进入</a>
          </td>
            </tr>
      </table>
    </div>
  </li>
</ul>
<!-- <div>dddd</div> -->
</template>

<script>
import Vue from 'vue'
import { InfiniteScroll } from 'mint-ui'
import data from '../libs/data'

Vue.use(InfiniteScroll);

export default {
    data() {
      return {
        list: [],
        loading: false,
        allLoaded: false,
        wrapperHeight: 0,
        page:1
      };
    },
    props:['selected'],
    mounted() {
      console.log(this.selected);
      //this.wrapperHeight = document.documentElement.clientHeight - this.$refs.wrapper.getBoundingClientRect().top;
      // for (let i = 1; i <= 20; i++) {
      //   this.list.push(i);
      // }      
    },
    computed: {
      scrollDisabled(){
        return (!this.selected||this.loading)
      }
    },
    methods: {
      loadMore() {        
        var _this = this;
        //console.log(this.loading);
        if(this.loading)return;
        this.loading = true;    
        console.log('444444444444');
        data.getHotGames(this.page).then((response) => {          
            var data = eval('('+response.data+')').data;           
            for (let i = 0; i < data.length; i++) {                       
              this.list.push(data[i]);
            }
            this.page += 1;
            setTimeout(function(){_this.loading = false;},2000)            
        }, (response) => {
            // 响应错误回调
        });
      }
    },
    watch: {
      selected(val){ 
        //console.log(this.list.length);
        if(this.selected && this.list.length == 0){          
          this.loadMore();
        }
      }
    }
    
  };
</script>

<style scoped>
  li.new-service {
    padding: 0;
    height: 40px;
    font-size: 12px;
  }
  
  .new-service td {
    padding-right: 5px;
    padding-left: 5px;
  }

  li.new-service td a {
    float: left;
    display: inline-block;
    background-color: #f2f2f2;
    color: #5d5d5d;
    padding: 3px 9px;
    border-color: #e4e4e4;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 12px;
  }
</style>