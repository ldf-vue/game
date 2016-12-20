<template>
    <div id="lastPlay" :class={hasPlay:hasPlay}>
    	<p class="play-title">最近在玩</p>

    	<div class="play-list">
    		<ul>
    			<li v-for="item in items">
    				<a class="games">
    					<img v-bind:src="item.img">
    					<p>{{ item.info }}</p>
    				</a>
    			</li>
    		</ul>
    	</div>
    </div>
</template>


<script>
import Vue from 'vue'


export default {
  name: 'lastPlay',
  data () {
    return {
      msg: 'myHeader.vue',
      hasPlay: true,
       items: [
        {img:'http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif', info:'妖怪宝可萌'},
        {img:'http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif', info:'妖怪宝可萌'},
        // {img:'http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif', info:'妖怪宝可萌'},
        // {img:'http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif', info:'妖怪宝可萌'},
        // {img:'http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif', info:'妖怪宝可萌'},
        // {img:'http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif', info:'妖怪宝可萌'},
        // {img:'http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif', info:'妖怪宝可萌'},
        // {img:'http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif', info:'妖怪宝可萌'},
      ],
    }
  }
}
</script>


<style type="text/css" scoped>
	#lastPlay {
		height: 115px;
		/*margin: 1px 0;*/
		display: none;
		background: #fff;
	}

	#lastPlay.hasPlay {
		display: block;
	}

	.play-title {
		background: #efeff4;
		padding-left: 16px;
	    font-weight: 400;
	    font-size: 13px;
	    color: #9f9f9f;
	    padding-top: 6px;
	    padding-bottom: 4px;
	}


	.play-list {
	    position: relative;
	    z-index: 1;
	    height: 90px;
	    width: 100%;
	    background: #fff;
	    overflow: hidden;
	}
	.play-list ul {
		padding: 0;
		margin: 0;
	    
        overflow: auto;
		white-space: nowrap;
		-webkit-transform: translateZ(0);
		-moz-transform: translateZ(0);
		-ms-transform: translateZ(0);
		-o-transform: translateZ(0);
		transform: translateZ(0);
	}
	.play-list li {
	    width: 80px;
		height: 90px;
		/*float: left;*/
		display: inline-block;
		background-color: #fff;
		overflow: hidden;
		text-align: center;
	}
	.play-list li a {
	    display: inline-block;
	    width: 100%;
	    height: 100%;
	}
	.play-list li img {
		width: 50px;
	    height: 50px;
	    margin-top: 10px;
	}
	.play-list li p {
		font-size: 11px;
	    margin-top: 5px;
	    margin-bottom: 0;
	    color: #1f1f1f;;
	}
</style>