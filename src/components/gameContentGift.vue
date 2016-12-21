<template>
    <div id="gameContentGift">
      <div class="game-desc">
        <p class="section-title">礼包</p>
      </div>

    	<div class="game-gift">
        
        <div v-for="item in items" class="gift-list">
          <div class="gift-title">疯狂游乐场新手礼包</div>
          <p class="gift-desc">元宝*150，虎符*2，金币*500000，刷新符*3，喇叭*2
礼包使用方法：在“主城”界面，点击“激活码”按钮，输入兑换码领取奖励点穿v大发v大发水电费士大夫似的发士大夫士大夫似的飞士大夫似的发士大夫水电费水电费</p>
          <div class="gift-progress">
            <div class="gift-progress-bar" style="width: 32%"></div>
          </div>
          <p class="gift-remain">剩余:32%</p>
          <span class="get">领 取</span>
        </div>
        
      </div>
    </div>
</template>

<script>
import Vue from 'vue'


export default {
  name: 'gameContentGift',
  data () {
    return {
      msg: 'gameContentGift.vue',
      items: [
        {},
        {}
      ],
    }
  }
}
</script>


<style type="text/css" scoped>
	.gift-list {
    position: relative;
    background-color: #fff;
    border-top: 1px solid #ddd;
  }

  .gift-title {
    margin: 8px 5px 0 10px;
    font-size: 15px;
  }
  .gift-desc {
    width: 70%;
    margin: 0 5px 3px 10px;
    font-size: .8em;
    line-height: 1.2;
    color: #999;
  }
  .gift-remain {
    padding: 3px 5px 3px 10px;
    font-size: .85em;
    color: #999;
  }
  .gift-progress {
    max-width: 70%;
    overflow: hidden;
    display: block;
    margin-left: 10px;
    height: 10px;
    background-color: #f5f5f5;
    border-radius: 2px;
    -webkit-box-shadow: inset 0 1px 2px rgba(0,0,0,.1);
    box-shadow: inset 0 1px 2px rgba(0,0,0,.1);
  }
  .gift-progress-bar {
    float: left;
    width: 0;
    height: 100%;
    font-size: 12px;
    line-height: 10px;
    background-color: #2697FC;
    -webkit-box-shadow: inset 0 -1px 0 rgba(0,0,0,.15);
    box-shadow: inset 0 -1px 0 rgba(0,0,0,.15);
    -webkit-transition: width .6s ease;
    -o-transition: width .6s ease;
    transition: width .6s ease;
  }
  .game-gift .get {
    vertical-align: middle;
    display: inline-block;
    position: absolute;
    color: #777;
    right: 10px;
    top: 33px;
    background-color: #fff;
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 6px 12px;
    font-size: 14px;
    line-height: 1.42857143;
  }
</style>