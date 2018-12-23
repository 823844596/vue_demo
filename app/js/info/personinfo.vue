<template>
  <div>
    <section :class="$style.header">
      <img src='//img12.360buyimg.com/jrpmobile/jfs/t2644/238/1420176553/1442/96e2885/573d96deN06201af5.png' />
      <em>会员福利</em>
    </section>
    <div :class="$style.listContainer">
    <section :class="$style.content" v-for="item in list" :key="item.icon">
      <img :src="item.icon" />
      <span :class="$style.text">{{item.text}}</span>
      <em :class="$style.link">{{item.link}}</em>
    </section>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      list: [
        {
          icon: '//img12.360buyimg.com/jrpmobile/jfs/t8971/199/1863233880/2035/56d04776/59cb5fbdNa7c682c3.png?width=70&height=70',
          text: '我的资产',
          link: '查看全部资产'
        },
        {
          icon: '//img12.360buyimg.com/jrpmobile/jfs/t8836/18/2342020923/2120/a9b7a8ff/59cb6124N31cb2889.png?width=70&height=70',
          text: '我的优惠券',
          link: '查看全部'
        },
        {
          icon: '//img12.360buyimg.com/jrpmobile/jfs/t10264/48/2521964269/2177/cb479501/59f945edNc1197b64.png?width=90&height=90',
          text: '我的金币',
          link: '赚金币兑好物'
        },
        {
          icon: '//img12.360buyimg.com/jrpmobile/jfs/t12115/250/469950434/3906/ad97c994/5a0bdf3aN22efb724.png?width=90&height=90',
          text: '我的金条',
          link: '查看额度'
        },
        {
          icon: '//img12.360buyimg.com/jrpmobile/jfs/t9244/132/2364556535/1134/334cd5d9/59cb612dN5b974dc5.png?width=70&height=70',
          text: '我的借钱',
          link: '查看全部产品'
        },
        {
          icon: '//img12.360buyimg.com/jrpmobile/jfs/t9121/110/2300703915/1348/91af205c/59cb613bN1e749e58.png?width=70&height=70',
          text: '我的白条',
          link: '去提额'
        }
      ]
    }
  }
}
</script>
<style lang="scss" module>
  @import '../../css/element.scss';
  .header{
    @include flex(row);
    justify-content: space-between;
    height: 140px;
    line-height: 140px;
    background-color: #fff;
    margin-bottom: 20px;
    >img{
      width: 100px;
      height: 100px;
      border-radius: 50%;
      margin: 20px 32px 0;
    }
    >em{
      font-size: 28px;
      color: #999;
      margin-right: 24px;
    }
  }
  .listContainer{
    @include flex(column);
    flex-wrap: nowrap;
    justify-content: space-between;
    justify-content: center;
    background-color: #fff;
    .content{
      @include flex(row);
      height: 112px;
      align-items: center;
      // border-bottom: 1px solid #ddd;
      &:after{
        content: " ";
        box-sizing: border-box;
        width: 100%;
        height: 2px;
        border-bottom: 1px solid #ddd;
        margin-left: 96px;
      }
      img{
        width: 48px;
        height: 48px;
        margin: 32px;
      }
      .text{
        font-size: 32px;
        color: #333;
        display: block;
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
      }
      .link{
        font-size: 28px;
        color: #999;
        position: absolute;
        right: 24px;
      }
    }
  }
</style>


