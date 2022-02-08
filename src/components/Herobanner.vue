<template>
  <section class="hero">
    
    <div class="general_bar">
      <div class="sx_content">
        <img src="../assets/avada-music-logo-retina.png">
      </div>

      <div class="right_content">
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
    
    <Strip
    :testo="campo"
    />
  </section>
</template>

<script>
import Strip from './partials/strip.vue' 

export default {
  name: 'Herobanner',
  components:{
    Strip
  },
  data() {
    return {
      campo: "ciao"
    }
  }

}
</script>

<style scoped lang="scss">
.hero
{
  background-color: lightcoral;

  .general_bar
  {
      display: flex;
      justify-content: space-between;
      align-items: center;
      border: 1px solid #010101;
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
    border: 1px solid blue;


    .content 
    {
      display: flex;
      flex-direction: column;
      justify-content: center;
      border: 1px solid green;
    }
  }
}  
</style>
