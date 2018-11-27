<template>
  <Panel title='新手特权' :class='$style.panel'>
    <section :class='$style.content'>
      <div :class='$style.item'>
        <h4>下载APP<span :class='$style.red'>送888元礼包</span></h4>
        <p :class="$style.gray">新手专享</p>
        <img src='https://img12.360buyimg.com/jrpmobile/jfs/t27088/243/2089650291/12365/2469f395/5bf677f9N795eec5e.png?width=120&height=120' />
      </div>
      <div :class='$style.item'>
        <!-- 以下内容不抽去组件原因：1.结构简单，没有复杂交互；2.数据不会经常改变 -->
        <ul>
          <li>
            <img src='https://img12.360buyimg.com/jrpmobile/jfs/t27088/243/2089650291/12365/2469f395/5bf677f9N795eec5e.png?width=120&height=120' />
            <h4>领128元新手礼包</h4>
            <p :class="$style.gray">立即开通</p>
          </li>
          <li>
            <img src='https://img12.360buyimg.com/jrpmobile/jfs/t27088/243/2089650291/12365/2469f395/5bf677f9N795eec5e.png?width=120&height=120' />
            <h4>打白条<span :class='$style.red'>享免息</span></h4>
            <p :class="$style.gray">立即开通</p>
          </li>
        </ul>
      </div>
    </section>
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
    >h4{
      border-bottom: 1px solid #ddd;
    }
    .content{
      @include list(row);
      .item{
        width: 50%;
        box-sizing: border-box; // css 盒模型计算宽度
        &:first-child{
          padding: 32px 20px;
          text-align: center;
          border-right: 1px solid #ddd;
          img{
            width: 132px;
            height: 132px;
            margin: 20px auto 0;
          }
        }
        h4{
          font-size: 26px;
          line-height: 40px;
        }
        .read{
          color: red;
        }
        .gray{
          color: #999;
          font-size: 24px;
        }
        p{
          margin-top: 6px;
          font-size: 24px;
        }
        ul{
          width: 100%;
          li{
            height: 144px;
            width: 100%;
            padding: 32px 28px;
            box-sizing: border-box;
            &:first-child{
              border-bottom: 1px solid #ddd;
            }
            h4{
              white-space: nowrap;
              text-overflow: ellipsis;
              overflow: hidden;
              text-align: left;
            }
            img{
              float: right;
              width: 80px;
              height: 80px;
            }
          }
        }
      }

    }
  }
</style>

