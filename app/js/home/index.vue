<template>
    <div>
       <Heador />
       <Silder />
       <Novice />
       <Borrow />
       <Money />
       <Product />
       <Life />
       <Footer />
       <Navbar />
    </div>
</template>

<script>
// Header未关键字，所以把Header改写未Heador
import Heador from '../public/header.vue';
import Navbar from '../public/navbar.vue'
import Silder from './hslider.vue';
import Novice from './novice.vue';
import Borrow from './borrow.vue'
import Money from './money.vue';
import Product from './product.vue';
import Life from './life.vue';
import Footer from '../public/footer.vue';
export default {
  components: {
    Heador,
    Silder,
    Novice,
    Borrow,
    Money,
    Product,
    Life,
    Footer,
    Navbar
  }
}
</script>

<style lang="scss" module>
  
</style>
