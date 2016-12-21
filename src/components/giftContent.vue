<template>
<div id="gift_list">
	<!-- 第一个循环体 -->
	<div class="list_item"  v-for="item in items">
		<!-- 模块头：游戏icon和游戏名 -->
	  <div class="item_title">
	    <img class="item_icon" :src="item.gameIcon">
	    <span class="item_name">{{item.gameName}}</span>
	  </div>
		<!-- 第二个循环体 -->
	  <div class="item_content" v-for="gift in item.gifts">
	  	<!-- 游戏礼包内容 -->
	    <div class="cont_title">
	      <span class="cont_name">{{gift.name}}</span>
	      <span class="cont_tip">通兑</span>
	      <p class="cont_disc">{{gift.disc}}</p>
	      <div class="cont_all">
	        <div class="cont_used"></div>
	      </div>
	      <p class="cont_used_text">{{gift.num}}</p>
	    </div>
	    <div class="item_btn">{{gift.btn}}</div>
	  </div>
	  <!-- 模块尾部更多礼包 不存在为none -->
	  <div :class="[item.moreClass]">
	    查看更多礼包（{{item.moreGift}}）
	    <span class="arr_right">></span>
	  </div>
	</div>
</div>
</template>

<script>
	export default {
  name: 'list_item',
  data () {
    return {
      items: [
        {
        	gameIcon:'http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif',
        	gameName:'妖怪宝可萌',
        	gifts: [
	        	{
	        		name:'独家豪华礼包',
	        		disc:'钻石 * 200 培养石 * 200 进化石 * 200',
	        		num:'已领取:TSLPMHHLB',
	        		btn:'查 看'
	        	},
	        	{
	        		name:'新手礼包',
	        		disc:'钻石 * 100 培养石 * 100 进化石 * 100',
	        		num:'此礼包不限领取数量',
	        		btn:'领 取'
	        	},
        	],
        	moreClass:'item_more',
        	moreGift:'2'},
        	{
        	gameIcon:'http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif',
        	gameName:'妖怪宝可萌',
        	gifts: [
	        	{
	        		name:'独家豪华礼包',
	        		disc:'钻石 * 200 培养石 * 200 进化石 * 200',
	        		num:'已领取:TSLPMHHLB',
	        		btn:'查 看'
	        	},
	        	{
	        		name:'新手礼包',
	        		disc:'钻石 * 100 培养石 * 100 进化石 * 100',
	        		num:'此礼包不限领取数量',
	        		btn:'领 取'
	        	},
        	],
        	moreClass:'none',
        	moreGift:''},
      ]
    }
  }
}
</script>

<style>
/*==============列表=============*/
.list_item {
  border-bottom: solid 1px #ddd;
  border-top: solid 1px #ddd;
  background-color: #fff;
  padding-bottom: 5px;
  margin-bottom: 10px
}
/*块头*/
.item_title {
  padding: 9px 10px 5px;
}
.item_icon {
  width: 50px;
  height: 50px;
  margin-right: 10px
}
.item_name {
  vertical-align: center;
  font-size: 14px;
  color: #333
}
/*内容区*/
.item_content,.item_more {
  border-top: 1px #ddd solid;
  margin-top: 5px;
  padding: 5px 10px 0 10px;
  position: relative;
}
/*.cont_title {
  width: 70%;
  display: inline-block;
}*/
.cont_name {
  font-size: 15px;
  color: #000;
  margin: 5px 0 1px 0;
}
.cont_tip {
  color: #C2955A;
  padding: 0 4px;
  border-radius: 4px;
  border: 1px solid #C2955A;
  margin-left: 4px;
  font-size: 10px;
  position: relative;
  top: -2px;
  font-family: 'Helvetica Neue',Arial,'Hiragino Sans GB','Microsoft Yahei','WenQuanYi Micro Hei',sans-serif;
}
.cont_disc {
  margin-bottom: 1px
}
/*进度条*/
.cont_all,.cont_used {
  max-width: 70%;
  overflow: hidden;
  display: block;
  height: 10px;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.cont_used {
  width: 32%;
  background-color: #2697FC;
}
.cont_used_text {
  font-size: .8em;
}
/*按钮*/
.item_btn {
  color: #777;
  position: absolute;
  right: 10px;
  top: 23px;
  padding: 6px 12px;
  border: solid 1px #ccc;
  border-radius: 4px;
  font-size: 14px;
}
/*列表尾部更多*/
.item_more {
  font-size: 14px;
  color: #333
}
.arr_right {
  float: right;
  color: #8c8c8c;
}
/*===========去掉某部分内容===================*/
.none {
  display: none
}
</style>