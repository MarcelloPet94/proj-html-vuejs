<template>
  <div id="app">
    <Herobanner v-for="(innerCont , i) in dataheropage" :key="i"
    :titolo="innerCont.titolo"
    :paragrafo="innerCont.paragrafo"
    :cta1="innerCont.cta1"
    :cta2="innerCont.cta2"
    />
    <Main/>
    <Videosection/>
    <Shopticket />
    <Footer/>
  
  </div>
</template>

<script>

import Footer from './components/Footer.vue'
import Herobanner from './components/Herobanner.vue'
import Main from './components/Main.vue'
import Shopticket from './components/Shopticket.vue'
import Videosection from './components/Videosection.vue'
import dataHero from './pageData/dataHero.js'

export default {
  name: 'App',
  components: {
    Herobanner,
    Main,
    Videosection,
    Shopticket,
    Footer,
  },
  data () {
    return {
      dataheropage: dataHero,
    }
  }
}
</script>

<style lang="scss">

@import './assets/style/global.scss';

</style>
