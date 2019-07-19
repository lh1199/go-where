<template>
  <div class="header">
    <div class="header-left">
      <i class="iconfont">&#xe624;</i>
    </div>
    <div class="header-input">
      <i class="iconfont">&#xe632;</i>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      城市
      <i class="iconfont" style="font-size: .12rem">&#xe64a;</i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
.header
  display: flex
  line-height: .86rem
  background: #00bcd4
  color: #fff
  .header-left
    width: .64rem
    float: left
  .header-input
    flex: 1
    margin-top: .12rem
    margin-left: .2rem
    padding-left: .1rem
    line-height: .64rem
    height: .64rem
    background: #fff
    border-radius: .1rem
    color: #ccc
    text-align: left
  .header-right
    width: 1.24rem
    float: right
    text-align: center
</style>


