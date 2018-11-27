<template>
  <Panel title='新品推荐' :class='$style.panel'>
    <section :class='$style.content'>
      <div :class='$style.arrow'>更多尖货></div>
      <Slider :options='options' :items="items" cname="product-slider" />
    </section>
  </Panel>
</template>
<script>
  import Panel from '../core/panel.vue';
  import Slider from '../core/slider.vue';
  export default {
    components: {
      Slider,
      Panel
    },
    data(){
      return {
        items: [
          {
            href: 'home',
            src: '//img12.360buyimg.com/jrpmobile/jfs/t28174/190/417131104/41529/80db7464/5bf24dd8Nc031dff3.jpg?width=335&height=421'
          },
          {
            href: 'home',
            src: '//img12.360buyimg.com/jrpmobile/jfs/t27892/325/1984931380/71410/61ed8546/5bf24deeNf7457c6f.jpg?width=335&height=421'
          },
          {
            href: 'home',
            src: 'https://img12.360buyimg.com/jrpmobile/jfs/t26245/260/1932008857/33085/5329fce8/5bf28c0aN70c40dfd.jpg?width=335&height=421'
          }
        ],
        options: {
          // pagination: {
          //   el: '.swiper-pagination',
          //   clickable: true
          // },
          paginationClickable: true,
          slidesPerView: 2.3,
          spaceBetween: 30,
          freeMode: true
        }
      }
    }
  }
</script>
<style lang="scss" module>
  @import '../../css/element.scss';
  .panel{
    @include panel;
    .content{
      padding-bottom: 40px;
      position: relative;
      &>div{
        position: absolute;
        font-size: 28px;
        color: #999;
        right: 20px;
        top: -70px;
      }
    }
  }
  
</style>
<style lang='scss'>
  /* 此处为第三方样式 */
  .product-slider{
    .swiper-container{
      box-sizing: border-box;
      padding: 0 24px;
      .swiper-slide{
        a{
          display: inline-block;
          width: 100%;
          img{
            width: 100%;
            display: block;
            height: 314px;
            border: 1px solid #fafafa;
          }
        }
      }
    }
  }
</style>

