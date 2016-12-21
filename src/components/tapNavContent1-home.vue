<template>  
<ul
  v-infinite-scroll="loadMore"
  infinite-scroll-disabled="scrollDisabled"
  infinite-scroll-distance="30">
  <li v-for="item in list">
    <a href="/#/details" class="gameDetails">
      <div>
        <img :src="item.icon"/>
      </div>   
      <div class="game-text">
        <div>
          <p>{{item.title}}</p>
          <span class="only" :class={show:item.showOnly}>独家</span>
          <span class="hot" :class={show:item.showHot}>热门</span>
          <span class="gift" :class={show:item.showGift}>礼包</span>
        </div>
        <p class="small">{{item.brief_intro}}</p>      
      </div>
    </a>

    <div class="right-enter">
      <a v-bind:href="item.href" class="btn">进入</a>
    </div>
  </li>
</ul>
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
        page:1
      };
    },
    props:['selected'],  
    computed: {
      scrollDisabled(){
        return (!this.selected||this.loading)
      }
    },
    methods: {
      loadMore() {
        var _this = this;
        if(this.loading)return;
        this.loading = true;    
        console.log('1111111111');
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
        if(this.selected && this.list.length == 0){          
          this.loadMore();
        }
      }
    }
    
  };
</script>

<style>
  .game-text p {
    display: inline-block;
  }

  .game-text span {
    margin-left: 4px;
    padding: 0 2px;
    font-size: 10px;
    border-radius: 2px;
    position: relative;
    top: -2px;
    display: none;
  }

  .game-text span.show {
    display: inline-block;
  }

  .game-text span.only {
    color: red;
    border: 1px solid red;
  }
  .game-text span.hot {
    color: orange;
    border: 1px solid orange;
  }
  .game-text span.gift {
    color: #2697FC;
    border: 1px solid #2697FC;
  }

  .right-enter {
    /*float: right;*/
    vertical-align: middle;
    transform: translateY(-50%);
    position: absolute;
    top: 50%;
    right: 10px;
  }

  .right-enter a.btn {
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
