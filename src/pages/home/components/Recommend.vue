<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1907/40/401b7b735008f7f4a3.img.jpg_200x200_10ce515e.jpg',
        title: '西溪国家湿地公园·周家村',
        desc: '西溪国家湿地公园·周家村西溪国家湿地公园·周家村'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1907/40/401b7b735008f7f4a3.img.jpg_200x200_10ce515e.jpg',
        title: '西溪国家湿地公园·周家村',
        desc: '西溪国家湿地公园·周家村西溪国家湿地公园·周家村'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1907/40/401b7b735008f7f4a3.img.jpg_200x200_10ce515e.jpg',
        title: '西溪国家湿地公园·周家村',
        desc: '西溪国家湿地公园·周家村西溪国家湿地公园·周家村'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '../../../assets/styles/mixins.styl'
.title
  margin-top: .1rem
  line-height: .8rem
  background: #eee
  text-indent: .2rem
.item
  display: flex
  overflow: hidden
  height: 1.9rem
  .item-img
    width: 1.7rem
    height: 1.7rem
    padding: .1rem
  .item-info
    flex: 1
    padding: .1rem
    min-width: 0
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
    .item-button
      line-height: .44rem
      margin-top: .16rem
      background: #ff9300
      padding: 0 .2rem
      border-radius: .06rem
      color: #fff
</style>


