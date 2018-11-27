<template>
  <!-- // 默认样式未btnClass， 如果不满足则通过props传入cname进行覆盖 -->
  <div :class="[btnClass, cname]">
    <slot />
  </div>
</template>

<script>
export default {
  props: {
    cname: {
      type: String,
      default: ''
    }
  },
  data(){
    return {
      btnClass: 'btn',

    }
  }
}
</script>

<style lang='scss'>
@import "../../css/element.scss";
.btn{
  @include btn;
}
</style>