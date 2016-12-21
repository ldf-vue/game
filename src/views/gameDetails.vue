<template>
    <div id="gameDetails">
    	<myHeader></myHeader>

    	<div class="game-header">
    		<img class="game-img" src="http://gc-img.oss-cn-qingdao.aliyuncs.com/sgqs_detalbanner-1479818245.jpg">
	    	<div class="game-bar"></div>
	    	<img class="game-icon" src="http://gc-img.oss-cn-qingdao.aliyuncs.com/sgqs_icon-1479818245.png">
	    	<p class="game-title">三国群神传</p>
	    	<p class="short-desc">群雄争霸，一统天下</p>
	    	<a class="start-game">开 始</a>
    	</div>

		<gameNav></gameNav>
    </div>
</template>

<script>
import Vue from 'vue'

import myHeader from '../components/myHeader'
import gameNav from '../components/gameNav-home'

export default {
  name: 'gameDetails',
  data () {
    return {
      msg: 'gameDetails.vue',
    }
  },
  components: { myHeader,gameNav }
}
</script>


<style type="text/css" scoped>
	.game-header {
		position: relative;
	   max-width: 100%;
	   height: 121px;
	}
	
	.game-img {
		widows: 100%;
		height: 100%;
		position: absolute;
	}
	.game-bar {
		position: absolute;
	    bottom: 0;
	    background-color: #000;
	    opacity: .5;
	    width: 100%;
	    height: 40px;
	}
	.game-icon {
	    position: absolute;
	    bottom: 4px;
	    left: 10px;
	    width: 55px;
	    height: 55px;
	}
	.game-title {
	    position: absolute;
	    bottom: 16px;
	    left: 72px;
	    color: #fff;
	    font-size: 1.2em;
	}
	.short-desc {
		position: absolute;
	    bottom: 3px;
	    left: 72px;
	    color: #fff;
	    font-size: .85em;
	}
	.start-game {
	    position: absolute;
	    bottom: 5px;
	    right: 15px;
	    padding: 3px 15px;
	    font-size: 1em;
	    line-height: 1.5;
	    border-radius: 3px;
        color: #fff;
	    background-color: #5cb85c;
	    border-color: #4cae4c;
	    display: inline-block;
		margin-bottom: 0;
		font-weight: 400;
		text-align: center;
		vertical-align: middle;
    	cursor: pointer;
	}
</style>