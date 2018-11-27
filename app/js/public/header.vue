<template>
   <!-- 1.dom结构； 2.图片：采用背景图方式，减少http请求；3.布局方式：左右浮动、flex、table-cell -->
  <div :class="$style.header">
    <span :class="$style.left">
      <em>注册</em>
      &nbsp;|&nbsp;
      <em>登陆</em>
    </span>
    <btn :class="$style.btnDownload">APP下载</btn>
  </div>
</template>
<script>
  import btn from '../core/btn.vue';
  export default{
    components: {
      btn
    }
  }
</script>
// style设定module， 开启css module
<style lang="scss" module>
  .header{
    color: #666;
    height: 100px;
    line-height: 100px;
    position: fixed;
    top: 0px;
    left: 0px;
    right: 0px; /* 通过制定left：0， right：0 将宽度变为100%*/
    font-size: 32px;
    background: #fff url('//m.jr.jd.com/spe/qyy/main/images/jr-logo.png') center center no-repeat;
    background-size: auto 50%;
    z-index: 100;
    .left{
      font-size: 28px;
      height: 30px;
      line-height: 30px;
      margin: 17px 0 0 18px;
    }
    .btnDownload{
      float: right;
      font-size: 24px;
      border-width: 0px;
      height: 56px;
      line-height: 56px;
      min-width: 120px;
      padding: 0;
      border-radius: 4px;
      margin: 28px 24px 0 0;
    }
  }
</style>