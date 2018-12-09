<template>
    <div>
       <Heador />
       <Silder />
       <Welfare />
       <Service />
       <Footer />
       <Navbar />
    </div>
</template>

<script>
// Header未关键字，所以把Header改写未Heador
import Heador from '../public/header.vue';
import Navbar from '../public/navbar.vue'
import Silder from './islider.vue';
import Welfare from './welfare.vue';
import Service from './service.vue';
import Footer from '../public/footer.vue';
export default {
  components: {
    Heador,
    Silder,
    Welfare,
    Service,
    Footer,
    Navbar
  }
}
</script>
