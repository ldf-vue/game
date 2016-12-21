<template>
<div id="gift">
  <myHeader></myHeader>
  <p class="gift_title">游戏礼包列表</p>
  <div class="gift_list">
    <div class="list_item">
      <div class="item_title">
        <img class="item_icon" src="http://gc-img.oss-cn-qingdao.aliyuncs.com/icon-1482070788.gif">
        <span class="item_name">妖怪宝可萌</span>
      </div>
      <div class="item_content">
        <div class="cont_title">
          <span class="cont_name">独家豪华礼包</span>
          <span class="cont_tip">通兑</span>
          <p class="cont_dic">钻石 * 200 培养石 * 200 进化石 * 200</p>
          <div class="cont_all">
            <div class="cont_used"></div>
          </div>
          <p class="cont_used_text">已领取:TSLPMHHLB</p>
        </div>
        <div class="item_btn">查 看</div>
      </div>
      <div class="item_content">
      <div class="cont_title">
          <span class="cont_name">独家豪华礼包</span>
          <span class="cont_tip">通兑</span>
          <p class="cont_dic">钻石 * 200 培养石 * 200 进化石 * 200</p>
          <div class="cont_all">
            <div class="cont_used"></div>
          </div>
          <p class="cont_used_text">已领取:TSLPMHHLB</p>
        </div>
        <div class="item_btn">查 看</div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import myHeader from '../components/myHeader'

export default {
  name: 'app',
  data () {
    return {      
    }
  },
  components: { myHeader }
}
</script>

<style>
#gift {
  font-size: 11px;
  color: #9f9f9f;
  font-family: '微软雅黑'
}
/*礼包界面主标题*/
.gift_title {
  margin: 20px 0 0 16px;
  padding: 4px 0;
}
/*==============列表=============*/
.gift_list {
  
}
.list_item {
  border-bottom: solid 1px #ddd;
  border-top: solid 1px #ddd;
  background-color: #fff;
  padding-bottom: 5px
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
.item_content {
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
</style>
