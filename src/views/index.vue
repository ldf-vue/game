<template>
    <div id="index">
      <myHeader></myHeader>
      <swipe></swipe>
      <lastPlay></lastPlay>
      <tapNav></tapNav>      
    </div>
</template>

<script>
import myHeader from '../components/myHeader'
import lastPlay from '../components/lastPlay'
import swipe from '../components/swipe-home'
import tapNav from '../components/tapNav-home'

export default {
  name: 'app',
  data () {
    return {      
    }
  },
  components: { myHeader,lastPlay,swipe,tapNav }
}
</script>

<style>
body{
  background: #f5f5f5
}
#app{
  padding-bottom: 51px;
}
</style>
