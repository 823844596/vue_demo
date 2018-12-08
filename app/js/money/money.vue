<template>
  <Panel title='理财精选' :class="$style.panle">
    <section :class="$style.content">
      <!-- 循环四次，出现列表 -->
      <dl :class="$style.item" v-for="item in items" :key="item.title">
        <dt>{{item.title}}<span :class="$style.red">{{item.sub}}</span></dt>
        <dd>{{item.rate}}</dd>
        <dd>{{item.text}}</dd>
      </dl>
    </section>
  </Panel>
</template>
<script>
  import Panel from '../core/panel.vue';
  export default {
    components: {
      Panel
    },
    data(){
      return {
        items: [
          {
            title: '定期理财',
            sub: '理财首选',
            rate: '5.60%',
            text: '历史年华回报率'
          },
          {
            title: '京智0号',
            sub: '大数据赋能',
            rate: '6。00%',
            text: '近1月历史年化投资回报率'
          },
          {
            title: '小白基金',
            sub: '超短期',
            rate: '4.50%',
            text: '7日年化收益率'
          },
          {
            title: '建信养老飞益鑫',
            sub: '1000起投',
            rate: '4.70%',
            text: '7日年化收益率'
          }
        ]
      }
    }
  }

</script>
<style lang="scss" module>
  @import '../../css/element.scss';
  .panle{
    @include panel;
    .content{
      @include list(row);
      justify-content: space-around;
      box-sizing: border-box;
      &:after{
        content: ' ';
        display: block;
        width: 100%;
        height: 0px;
        box-sizing: border-box;
        border-bottom: 1px solid #ddd;
        position: relative;
        top: -248px;      // 通过position：relative, 使用top改变偏移量，将最下面的线移动到中间
      }
      .item{
        position: relative;
        width: 50%;
        padding: 34px 16px;
        box-sizing: border-box;
        &:after{
          content: ' ';
          width: 1px;
          height: 136px;
          position: absolute;
          top: 50%;
          right: 0;
          margin-top: -68px;
          border-right: 1px solid #eee;
        }
        &:nth-child(2n){
          &:after{
            display: none;
          }
        }
        dt{
          font-size: 30px;
          line-height: 42px;
          color: #333;
          span{
            font-size: 22px;
            color: #ff5155;
            border: 1px solid #ff5155;
            padding: 0 8px;
            vertical-align: 1px; // 通过该属性调整base-line对齐方式
            margin-left: 2px;
          }
        }
        dd{
          &:nth-child(2){
            font-weight: 700;
            font-size: 44px;
            height: 58px;
            line-height: 58px;
            color: #FF5155;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
          }
          &:nth-child(3){
            font-size: 24px;
            height: 34px;
            line-height: 34px;
            color: #999;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
          }
        }
      }
    }
  }
</style>
