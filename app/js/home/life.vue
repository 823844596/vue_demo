<template>
  <Panel title='生活服务' :class="$style.panel">
    <ul :class='$style.content'>
      <li :class="$style.item">
        <img src='//img12.360buyimg.com/jrpmobile/jfs/t1/3924/28/657/3552/5b9240dbE60256c31/78b52d5ab675f800.png?width=90&height=90' />
        <p>惠加油</p>
      </li>
      <li :class="$style.item">
        <img src='//img12.360buyimg.com/jrpmobile/jfs/t1/1216/39/659/4516/5b923b1cE5943d1c6/dabaf8b842f57eb9.png?width=90&height=90//img12.360buyimg.com/jrpmobile/jfs/t27088/243/2089650291/12365/2469f395/5bf677f9N795eec5e.png?width=120&height=90' />
        <p>小白信用</p>
        <p>全新升级</p>
      </li>
      <li :class="$style.item">
        <img src='//img12.360buyimg.com/jrpmobile/jfs/t1/520/34/950/3686/5b9239e3Eaaf5465c/8d8c35badacfc114.png?width=90&height=90' />
        <p>卡转让</p>
      </li>
      <li :class="$style.item">
        <img src='//img12.360buyimg.com/jrpmobile/jfs/t1/3924/28/657/3552/5b9240dbE60256c31/78b52d5ab675f800.png?width=90&height=90' />
        <p>惠加油</p>
      </li>
      <li :class="$style.item">
        <img src='//img12.360buyimg.com/jrpmobile/jfs/t1/3924/28/657/3552/5b9240dbE60256c31/78b52d5ab675f800.png?width=90&height=90' />
        <p>示例图</p>
      </li>
    </ul>
  </Panel>
</template>
<script>
  import Panel from '../core/panel.vue';
  export default {
    components: {
      Panel
    }
  }
</script>
<style lang="scss" module>
  @import '../../css/element.scss';

  .panel{
    @include panel;
    .content{
      @include list(row);
      box-sizing: border-box;
      padding-bottom: 40px;
      .item{
        width: 20%;
        text-align: center;
        img{
          width: 90px;
          height: 90px;
        }
        p{
          font-size: 26px;
          color: #666;
          text-overflow: ellipsis;
          white-space: nowrap;
          overflow: hidden;
          margin-top: 12px;
          &:nth-child(3){
            color: #ff801a;
          }
        }
      }
    }
  }
</style>
