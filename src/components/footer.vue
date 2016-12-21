<template>
  <div id="footer">
    <ul class="box-flex">
      <li v-for="item in items" class="box-flex-item">
        <router-link v-if="item.href.indexOf('http:')==-1" :to="{ name: item.href}" :class="{'on':item.href==curHref}">
          <i class="iconfont" :class="[item.class]"></i>
          <p>{{item.name}}</p>
        </router-link>
        <a v-else :href="item.href">
          <i class="iconfont" :class="[item.class]"></i>
          <p>{{item.name}}</p>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'footer',
  data () {
    return {
      items: [
        {name:'游戏',class:'icon-zhuye',href:'home'},
        {name:'礼包',class:'icon-kefu',href:'gift'},
        {name:'社区',class:'icon-jilu',href:'http://buluo.qq.com/mobile/barindex.html?_bid=128&_wv=1027&bid=240598'},
        {name:'个人',class:'icon-zhangdan1',href:'person'}
      ],
      curHref:'home'
    }
  },
  watch: {
    // 如果路由有变化，会执行该方法
    '$route': 'routeChange'
  },
  methods: {
    routeChange () {
      if(this.$route.name != 'details') {
        this.curHref = this.$route.name;
        document.getElementById('footer').style.display = 'block';
      } else {
        document.getElementById('footer').style.display = 'none';
      }
    }
  }
}
</script>

<style scoped>
#footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 50px;
  background: #fff;
  border-top: 1px solid #ddd;
}
ul,li{
  height: 100%;
}
a{
  display: inline-block;
  height: 100%;
  width: 100%; 
  box-sizing: border-box;
  padding-top: 2px;
  text-align: center;
}
a.on{
  color: red;
}
</style>
