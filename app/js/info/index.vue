<template>
  <div>
    <PersonInfo />
     <Navbar />
  </div>
</template>
<script>
  import PersonInfo from './personinfo.vue' 
  import Navbar from '../public/navbar.vue';
  export default {
    components: {
      PersonInfo,
      Navbar
    }
  }
</script>

