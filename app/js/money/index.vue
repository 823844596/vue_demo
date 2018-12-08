<template>
    <div>
       <Heador />
       <Silder />
       <Ada />
       <Money />
       <Adb />
       <Finance />
       <Adc />
       <Footer cname='$style.mfooter'/>
       <Navbar />
    </div>
</template>

<script>
// Header未关键字，所以把Header改写未Heador
import Heador from '../public/header.vue';
import Navbar from '../public/navbar.vue'
import Silder from './mslider.vue';
import Footer from '../public/footer.vue';
import Ada from './ada.vue'
import Money from './money.vue';
import Adb from './adb.vue';
import Finance from './finance.vue'
import Adc from './adc.vue'
export default {
  components: {
    Heador,
    Silder,
    Footer,
    Navbar,
    Ada,
    Money,
    Adb,
    Finance,
    Adc
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
