<template>
  <section class="hero">

      <nav :class="{openNav : this.navState}" class="hover_menu_nav">
        <div class="general_bar">
          <div class="sx_content">
            <img src="../assets/avada-music-logo-retina.png">
          </div>

          <div class="right_content" @click="burgerOpen">
            <i class="fas fa-close" style="color:#fefefe"></i>
          </div>
        </div>    

        <div class="txt_content_block">
            <div class="content">
                <div v-for="(inner, index) in vocimenu" :key="index">
                  <a class="navhover" :href="inner.href">
                      {{inner.voce}}
                  </a>
                </div>
            </div>  
        </div>          
      </nav>
    <div class="bg">
      <div class="general_bar">
        <div class="sx_content">
          <img src="../assets/avada-music-logo-retina.png">
        </div>

        <div class="right_content" @click="burgerOpen">
          <i class="fas fa-bars" style="color:#fefefe;"></i>
        </div>
      </div>

      <div class="txt_content_block">
          <div class="content">
            <h1 class="heroText">{{titolo}}</h1>
            <p class="emotionalText">{{paragrafo}}</p>
            <div class="cta">
              <a class="cta_first" href="#">{{cta1}}</a>
              <a class="cta_base" href="#">{{cta2}}</a>
            </div>
          </div>  
      </div>
    </div>  
    
    <Stripseo
    :testo="campo"
    :paragrafo = "parInfo"
    />
  </section>
</template>

<script>
import Stripseo from './partials/Stripseo.vue' 

export default {
  name: 'Herobanner',
  components:{
    Stripseo
  },

  props: {
    titolo: String,
    paragrafo: String,
    cta1: String,
    cta2: String,
  },

  data() {
    return {
      navState : false,
      campo: "Music is Life",
      parInfo: "Music is Life",
      vocimenu: [
        {
          'voce': 'Home',
          'href': '#'
        },
        {
          'voce': 'Meet The Band',
          'href': '#' 
        },
        {
          'voce': 'Live Dates',
          'href': '#livedate' 
        },
        {
          'voce': 'Latest News',
          'href': '#' 
        },
        {
          'voce': 'Albums',
          'href': '#' 
        },
        {
          'voce': 'Fans',
          'href': '#' 
        }                                                                     
      ]
    }
  },

  methods: {
    burgerOpen()
    {
      this.navState = !this.navState
    }
}

}
</script>

<style scoped lang="scss">
@import '../assets/style/variable.scss';
@import '../assets/style/general.scss';

.hero
{
  position: relative;
  background-color: $midgray;


  .openNav {display: block !important;}

  .hover_menu_nav
  {
    display: none;
    position: absolute;
    top: 0;
    width: 100%;
    min-height: 100vh;
    height: 100vh;
    background-color: $mandy;
    z-index: 2;

    .navhover:hover
    {
      opacity: 1;
    }
  }
  
  .bg
  {
      background-image: url(../assets/home_slider.jpg);
      background-position: center center;
      background-size: 100%;
  }

  .general_bar
  {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 24px;

      .sx_content
      {
          width: 200px;

          img
          {
            width: 100%;
          }
      }

      .right_content
      {
        cursor: pointer;
      }
  }


  .txt_content_block
  {
    display: flex;
    justify-content: center;
    align-content: center;
    height: 90vh;
    text-align: center;


    .content 
    {
      display: flex;
      flex-direction: column;
      justify-content: center;

      .cta_base:hover
      {
        color: $charade;
        border: 1px solid $charade;
        background-color: $white;
      }
    }
  }
}  


</style>
