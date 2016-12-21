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
    <tapNav></tapNav>
  </div>
</template>

<script>

import tapNav from '../components/tapNav-person'

export default {
  name: 'person',
  data () {
    return {      
    }
  },
  components: { tapNav }
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

</style>
