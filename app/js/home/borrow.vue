<template>
  <Panel title='极速借贷' :class="$style.panelContainer">
    <section :class="$style.content">
      <router-link :to="{name: 'home', params: {}}">
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t12355/171/849656870/29064/92c9bc12/5a153643N04efba6e.jpg?width=210&height=260" />
      </router-link>      
    </section>
  </Panel>
</template>

<script>
  import Panel from '../core/panel.vue'
  export default {
    components: {
      Panel
    }
  }
</script>
<style lang="scss" module>
  @import '../../css/element.scss';
  .panelContainer{
    @include panel;
    .content{
      padding-bottom: 40px;
      img{
        display: block;
        width: 100%;
        height: 300px;
      }
    }
  }
</style>


