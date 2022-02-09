<template>
  <div id="app">
    <Herobanner/>
    <Main/>
    <Videosection/>
    <Shopticket/>
    <Footer/>
  </div>
</template>

<script>

import Footer from './components/Footer.vue'
import Herobanner from './components/Herobanner.vue'
import Main from './components/Main.vue'
import Shopticket from './components/Shopticket.vue'
import Videosection from './components/Videosection.vue'

export default {
  name: 'App',
  components: {
    Herobanner,
    Main,
    Videosection,
    Shopticket,
    Footer,
  }
}
</script>

<style lang="scss">

@import './assets/style/global.scss';

</style>
