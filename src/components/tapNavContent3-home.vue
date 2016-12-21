<template>  
<ul
  v-infinite-scroll="loadMore"
  infinite-scroll-disabled="scrollDisabled"
  infinite-scroll-distance="30">
  <li v-for="item in list" class="news">
    <div class="news-list">
      <div class="news-info">
        <div class="test-ellipsis">
          <span class="activity">活动</span>
          <!-- <p class="news-title">{{ item.title}}</p> -->
          <span class="news-title">《妖怪宝可萌》12月20日维护公告</span>
        </div>
      </div>
      <div class="news-time">
        <p>12-19</p>
      </div>
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
        console.log('3333333333');
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

<style>
  .news-info {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  li.news {
    height: 19px;
    padding: 9px;
    line-height: 19px;
    background:#fff;
    margin-top: 5px;
    position: relative;
  }
  .news-list .activity {
    padding: 2px;
    font-size: 10px;
    border-radius: 2px;
    position: relative;
    top: -2px;
    color: #2697FC;
    border: 1px solid #2697FC;
    height: 37px;
  }
  .news-info {
    width: 80%;
    float: left;
  }
  .news-title {
    display: inline;
    font-size: 14px;
  }
</style>
