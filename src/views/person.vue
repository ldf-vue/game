<template>
  <div id="person">
    <div id="head">
      <span class="id">ID:12345678</span>
      <div id="user_img">
        <img class="user_img" src="http://wx.qlogo.cn/mmopen/PiajxSqBRaELcVDXr1DF5Eovn3UbJnKGW4RhoG6aqD0fWI7TUibUPmJTOzmcsnibVsicUdzzrM8ibkBtn28EQ7GLkrw/0">
      </div>
      <div id="user_name"><p>username</p></div>
      <div id="user_level"><img src="../assets/img/star.png"></div>
      <div id="user_exp"><p>经验:0/50</p></div>
      <a class="level_exp" href="#">等级说明</a>
    </div>
    <ul id="person_nav">
      <li class="recent">
       <span class="on">最近在玩</span>
      </li>
      <li class="set">
        <span class="">推送设置</span>
      </li>
    </ul>
    <div id="list">
      <div class="list_item">
        <div class="item_icon">
          <a href="#">
            <img class="icon" src="http://h5.hortorgames.com/gc/img/games/chuanqishijie_icon.png">
          </a>
        </div>
        <div class="item_text">
          <p class="title">传奇世界</p>
          <p class="load_time">上次登陆: 2016-12-19 17:22:35</p>
        </div>
        <div class="item_btn">
          <a href="#">进 入</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>



export default { 
  name: 'app',
  data () {
    return {
      msg: '顶顶顶顶Welcome to Your Vue.js App'
    }
  },
  methods:{
  	
  }
}
</script>

<style>
#person {
  font-family: '微软雅黑'
}
/*==============头部样式====================*/
#head {
  width: 100%;
  height: 180px;
  background: linear-gradient(to bottom,#1273d8,#89dfef) 0 0/100% 100% no-repeat;
  position: relative;
}
/*抽取公共样式*/
.id,#user_name p,#user_exp p,.level_exp { 
  padding: 3px;
  color: #ddd;
  background-color: rgba(0, 0, 0, 0.4);
  border-radius: 5px;
}
/*用户id*/
.id {
  position: absolute;
  margin: 5px;
  top: 0;
  left: 0;
}
/*用户头像*/
#user_img {
  top: 20px;
  border: solid 2px #FFFFFF;
  margin: 0 auto;
  position: relative;
  top: 20px
}
#user_img,.user_img {
  width: 71px;
  height: 71px;
  border-radius: 50%;
}
/*用户名*/
#user_name {
  margin-top: 30px;
  text-align: center;
}
#user_name p,#user_exp p {
  padding: 2px 3px;
  display: inline-block; 
  text-align: center;
  font-size: 1.1em
}
/*用户等级*/
#user_level,#user_exp {
  margin-top: 2px;
  text-align: center;
  font-size: 0.8em
}
/*等级说明*/
.level_exp {
  position: absolute;
  bottom: 0;
  right: 0;
  font-size: .8em;
  margin: 5px;
  text-decoration: underline;
}
/*=================中部选项卡==================*/
#person_nav {
  width: 100%;
  height: 45px;
  background-color: #fff;
  overflow: hidden;
  /*line-height: 45px*/
}
#person_nav li {
  display: inline-block;
  color: #888;
  width: 49%;
  text-align: center;
  font-size: 1.1em;
  height: 45px
}
#person_nav li span {
  margin: 0 8px;
  padding: 10px 0;
  display: block;
  text-align: center;
}
/*选择样式*/
.on {
  color: #2697FC;
  border-bottom: solid 2px #2697FC;
}
/*============最下方内容===============*/
#list {
  border-top: solid 1px #ddd;
  padding: 0 12px;
  background-color: #fff
}
.list_item {
  width: 100%;
  height: 60px;
  margin-top: 12px;
  padding-bottom: 5px
}
.item_icon,.item_text,.item_btn {
  display: inline-block;
  vertical-align: middle;
}
/*图标*/
.item_icon {
  padding-right: 10px;
}
.icon {
  width: 60px;
  height: 60px;
}
/*中间文字*/
.item_text {

}
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
.item_btn {
  float: right;
  padding-left: 10px;
}
.item_btn a {
  line-height: 60px;
  padding: 5px 13px;
  background-color: #f2f2f2;
  color: #5d5d5d;
  border: solid 1px #e4e4e4;
  border-radius: 3px;
  font-size: 12px
}
</style>
