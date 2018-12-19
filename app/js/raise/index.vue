<template>
    <div>
       <Heador />
       <Silder />
       <Daily />
       <In />
       <More />
       <Footer cname='$style.mfooter'/>
       <Navbar />
    </div>
</template>

<script>
// Header未关键字，所以把Header改写未Heador
import Heador from '../public/header.vue';
import Navbar from '../public/navbar.vue'
import Daily from './daily.vue';
import In from './in.vue';
import More from './more.vue';
import Silder from './rslider.vue';
import Footer from '../public/footer.vue';
export default {
  components: {
    Heador,
    Silder,
    Daily,
    In,
    More,
    Footer,
    Navbar
  }
}
</script>

<style lang="scss" module>
  .mfooter{
    margin-top: 0 !important;
    ul{
      li:first-child{
        display: none;
      }
    }
  }
</style>
