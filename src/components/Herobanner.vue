<template>
  <section class="hero">

      <nav :class="{openNav : this.navState}" class="hover_menu_nav">
        <div class="general_bar">
          <div class="sx_content">
            <img src="../assets/avada-music-logo-retina.png">
          </div>

          <div class="right_content" @click="burgerOpen">
            <i class="fas fa-close"></i>
          </div>
        </div>      
      </nav>

    <div class="general_bar">
      <div class="sx_content">
        <img src="../assets/avada-music-logo-retina.png">
      </div>

      <div class="right_content" @click="burgerOpen">
        <i class="fas fa-bars"></i>
      </div>
    </div>

    <div class="txt_content_block">
        <div class="content">
          <h1>Titolo</h1>
          <p>Lorem</p>
          <div class="cta">
            <a href="#">LATEST</a>
            <a href="#">LIVE DATES</a>
          </div>
        </div>  
    </div>
    
    <Stripseo
    :testo="campo"
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
  data() {
    return {
      navState : false,
      campo: "ciao"
    }
  },
    methods: {
    
    burgerOpen( )
    {
      this.navState = !this.navState
      console.log('ok')
    }

  }

}
</script>

<style scoped lang="scss">
.hero
{
  position: relative;
  background-color: lightcoral;


  .openNav {display: block !important;}

  .hover_menu_nav
  {
    display: none;
    position: absolute;
    top: 0;
    width: 100%;
    min-height: 100vh;
    height: 100vh;
    background-color:lightcoral;

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
    }
  }
}  


</style>
