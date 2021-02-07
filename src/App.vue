<template>
  <div id="app">
    <router-view/>
    <Footer/>
  </div>
</template>

<script>
import Footer from './components/common/Footer.vue'

export default {
  components:{
    Footer
  }
}
</script>

<style lang="scss">

#app{
  position: relative;
}
</style>
