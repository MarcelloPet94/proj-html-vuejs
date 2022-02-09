<template>
  <section class="footer">
    <div class="general_bar">
      <div class="sx_content">
        <img src="../assets/avada-music-logo-retina.png">
      </div>

      <div class="info_footer_content">
        <ul>
          <li><a href="#">voce</a></li>
          <li><a href="#">voce</a></li>
          <li><a href="#">voce</a></li>
        </ul>
      </div>
    </div>

    <div class="general_bar">
      <div class="sx_content">
      <div class="info_footer_content">
        <ul>
          <li><a href="#">voce</a></li>
          <li><a href="#">voce</a></li>
          <li><a href="#">voce</a></li>
        </ul>
      </div>
      </div>

      <div class="info_footer_icon">
        <a href="#" v-for="(icon , indice) in icons" :key="indice">
          <img :src="icon.social"/>
        </a>
      </div>
    </div>    
  </section>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      
      icons: [
        {
           'social' :  'https://img.icons8.com/ios-glyphs/30/000000/facebook-f.png',
        },
        {
           'social' :  'https://img.icons8.com/ios-glyphs/30/000000/twitter--v1.png',          
        },
        {
           'social' :  'https://img.icons8.com/ios/30/000000/instagram-new--v1.png',
        },
        {
           'social' :  'https://img.icons8.com/material/30/000000/youtube-play--v1.png',          
        }        
      ]

    }
  }
}
</script>

<style scoped lang="scss">

.footer  
  {
  background-color: darkblue;  

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
    
    .info_footer_content
    {

      ul
      {
        display: flex;
        color: #fff;

        li
        {
          list-style-type: none;

          a
          {
            color: #fff;
            padding: 16px;
          }
        }
      }
    }
    .info_footer_icon
    {
      a
      {
        width: 32px;
        height: 32px;
        background-color: #fff;        
        color: #fff;

      }
    }  
  }
</style>
