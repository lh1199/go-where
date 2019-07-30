<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '01',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '02',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/17/99402a22ce4af302.png',
        desc: '西湖'
      }, {
        id: '03',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        desc: '杭州必游'
      }, {
        id: '04',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png',
        desc: '漂流'
      }, {
        id: '05',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/17/99402a22ce4af302.png',
        desc: '印象西湖'
      }, {
        id: '06',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png',
        desc: '千岛湖'
      }, {
        id: '07',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
        desc: '浪浪水公园'
      }, {
        id: '08',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b8/c5dcdb58deec2402.png',
        desc: '西溪湿地'
      }, {
        id: '09',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
        desc: '杭州宋城'
      }, {
        id: '10',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png',
        desc: '杭州乐园'
      }],
      swiperOption: {
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      const pages = [];
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = []
        };
        pages[page].push(item)
      });
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '../../../assets/styles/varibles.styl'
@import '../../../assets/styles/mixins.styl'
.icons >>> .swiper-conteiner
  height: 0
  padding-bottom: 50%
.icon
  position: relative
  overflow: hidden
  float: left
  width: 25%
  height: 0
  padding-bottom: 25%
  .icon-img
    position: absolute 
    top: 0
    right: 0
    left: 0
    bottom: .44rem
    box-sizing: border-box
    padding: .1rem
    padding-bottom: 0
    .icon-img-content
      display: block
      margin: 0 auto
      height: 100%
  .icon-desc
    position: absolute 
    left: 0
    right: 0
    bottom: 0
    height: .44rem
    line-height: .44rem
    text-align: center
    color: $darkTextColor
    overflow: hidden
    white-space: nowrap
    ellipsis()
</style>


