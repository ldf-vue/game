<template>
<div id="per_list">
  <div class="per_list_item">
    <div class="per_item_icon">
      <a href="#">
        <img class="icon" src="http://h5.hortorgames.com/gc/img/games/chuanqishijie_icon.png">
      </a>
    </div>
    <div class="per_item_text">
      <p class="title">传奇世界</p>
      <p class="load_time">上次登陆: 2016-12-19 17:22:35</p>
    </div>
    <div class="per_item_btn">
      <a href="#">进 入</a>
    </div>
  </div>
</div>
</template>

<script>
export default {
name: 'per_list',
data () {
  return {
	  }
	}
}
</script>

<style>
#per_list {
  border-top: solid 1px #ddd;
  padding: 0 12px;
  background-color: #fff
}
.per_list_item {
  width: 100%;
  height: 60px;
  margin-top: 12px;
  padding-bottom: 5px
}
.per_item_icon,.per_item_text,.per_item_btn {
  display: inline-block;
  vertical-align: middle;
}
/*图标*/
.per_item_icon {
  padding-right: 10px;
}
.icon {
  width: 60px;
  height: 60px;
}
/*中间文字*/
.title {
  font-size: 17px;
  padding-top: 5px;
  color: #000;
  margin: 0 0 3px 0;
}
.load_time {
  font-size:  11px;
  color: #777;
  margin-bottom: 5px
 }
/*最后按钮*/
.per_item_btn {
  float: right;
  padding-left: 10px;
}
.per_item_btn a {
  line-height: 60px;
  padding: 5px 13px;
  background-color: #f2f2f2;
  color: #5d5d5d;
  border: solid 1px #e4e4e4;
  border-radius: 3px;
  font-size: 12px
}
</style>