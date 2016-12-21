<template>
    <div id="gameContentNwes">
    	<div class="game-desc">
    		<p class="section-title">游戏内容</p>
    		<p class="game-desc-content">
                在这里，您将扮演英明神武的主公，带领绝世名将，攻城略地，指引他们走向胜利。主公您将体验到全民PK的乐趣，与他人一较高下。也可以和武将一样，走上漫漫成神之路，成为别人口中的传说！古语乱世出英雄，我们为主公您准备了各种豪华大礼，超值礼包……军械库随时为主公您提供稀世装备，酒馆可为主公招揽名将，冒险可为主公探索到旷世宝物。主公您的战绩将被铭记在英雄殿上……来吧，主公，三国的战场就在这里等着您的来临！
            </p>
    	</div>

    	<div class="game-info">
    		<ul>
    			<li v-for="item in items">
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
    	</div>
    </div>
</template>

<script>
import Vue from 'vue'


export default {
  name: 'gameContentNwes',
  data () {
    return {
      msg: 'gameContentNwes.vue',
      items: [
      	{},
      	{},
      	{}
      ]
    }
  }
}
</script>


<style type="text/css">
	.section-title {
	    font-weight: 400;
	    font-size: 11px;
	    color: #9f9f9f;
	    padding-top: 4px;
	    padding-bottom: 4px;
	    margin: 0 0 0 16px;
	}
	.game-desc-content {
	    background-color: #fff;
	    border-top: 1px solid #ddd;
	    border-bottom: 1px solid #ddd;
	    font-size: .85em;
	    padding: 8px 5px 8px 10px;
	}
	
	.game-info {
		margin-top: 8px;
	}
	.game-info li {
		height: 19px;
	    padding: 9px;
	    line-height: 19px;
		margin-top: 2px;
	}
</style>