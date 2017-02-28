<template>
<div id="gift">
  <myHeader></myHeader>
  <p class="gift_title">游戏礼包列表</p>
  <giftContent></giftContent>
</div>
</template>

<script>
import myHeader from '../components/myHeader'
import giftContent from '../components/giftContent'

export default {
  name: 'app',
  data () {
    return {      
    }
  },
  components: { myHeader,giftContent }
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
</style>
