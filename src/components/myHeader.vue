<template>
    <div id="headWrap">
    	<div id="header">
			<div class="user-photo">
				<a href="/#/person">
					<img class="photo" v-bind:src="headImg">
				</a>
			</div>
			<p class="user-name">{{ userName}}</p>
			<p class="user-level">
				<img src="../assets/img/star.png">
			</p>

			<div id="appDownloap">
				<img src="../assets/img/waveiphone.gif" height="30" width="25">
				<span>下载APP</span>
			</div>
	    </div>
    </div>
</template>

<script>
import Vue from 'vue'


export default {
  name: 'myHeader',
  data () {
    return {
      msg: 'myHeader.vue',
      userName: '某某',
      headImg: 'http://wx.qlogo.cn/mmopen/PiajxSqBRaELcVDXr1DF5Eovn3UbJnKGW4RhoG6aqD0fWI7TUibUPmJTOzmcsnibVsicUdzzrM8ibkBtn28EQ7GLkrw/0',
    }
  }
}
</script>


<style type="text/css" scoped>
	#headWrap {
		position: relative;
	}
	#header {
	    height: 40px;
	    display: block;
	    background-color: #fff;
	    padding-left: 15px;
	    padding-right: 15px;
	    /*防止swipe滑动时页面跳动*/
	    /*margin: 1px 0;*/
	}
	.user-photo {
	    width: 50px;
	    height: 50px;
	    border-radius: 50%;
	    background-color: #fff;
	    box-shadow: 0 1px 1px rgba(0,0,0,.5);
	    padding: 2px;
	    position: absolute;
	    left: 10px;
	    top: 3px;
	    z-index: 2;
	    
	    /*防止swipe滑动时页面跳动*/
	    margin-top: 2px;
	    margin-left: 2px;

	    -webkit-box-sizing: border-box;
	    -moz-box-sizing: border-box;
	    box-sizing: border-box;
	}
	.user-photo .photo {
	    width: 46px;
		height: 46px;
		border-radius: 50%;
		vertical-align: middle;
		border: 0;
	}

	.user-name {
		margin: 0;
	    font-size: 1.1em;
	    position: absolute;
	    left: 75px;
	    top: 3px;
	    color: #444;
	    font-weight: 400;
    	letter-spacing: .4px;
    	font-size: 15px;
	}
	.user-level {
	    margin: 0;
	    font-size: .8em;
	    position: absolute;
	    left: 77px;
	    top: 21px;
	    color: #999;
	    letter-spacing: -3px;
	    vertical-align: middle;
	}

	#appDownloap {
		position: absolute;
    	right: 15px;
	    top: 0;
	    height: 40px;
	    line-height: 40px;
	    cursor: pointer;
	}
	#appDownloap span {
		font-size: 13px;
	    position: relative;
	    text-decoration: underline;
	    color: #2b95df;
	    top: 4px;
	}
</style>