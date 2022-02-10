<template>
  <section class="footer">
    <div class="general_bar">
      <div class="sx_content">
        <img src="../assets/avada-music-logo-retina.png">
      </div>

      <div class="info_footer_content">
        <ul>
          <li v-for="(showthis , indice) in vocimenu" :key="indice"><a :href="showthis.href">{{showthis.voce}}</a></li>
        </ul>
      </div>
    </div>

    <div class="general_bar">
      <div class="sx_content">
      <div class="info_footer_content">
        <ul>
          <li>
            <a href="#">@copyright&nbsp;2021&nbsp;-&nbsp;2020</a>
          </li>
          <li>
            <a href="#">AVADA&nbsp;THEME&nbsp;BY&nbsp;THEMEFUSION</a>
          </li>
          <li>
            <a href="#">ALL&nbsp;RIGHT&nbsp;RESERVED</a>
          </li>
          <li>
            <a href="#">POWERED&nbsp;BY&nbsp;WORDPRESS</a>
          </li>                                        
        </ul>
      </div>
      </div>

      <div class="info_footer_icon">
        <div v-for="(icon , indice) in icons" :key="indice">
          <a :href="icon.url">
            <i :class="icon.social"></i>
          </a>
        </div>
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
        {'social' : 'fab fa-facebook' , 'url' : "#"},
        {'social' : 'fab fa-twitter' , 'url' : "#"},
        {'social' : 'fab fa-instagram' , 'url' : "#"},
        {'social' : 'fab fa-youtube' , 'url' : "#"}
      ],
      vocimenu: [
        {
          'voce': 'Home',
          'href': '#',
          'copyright': '@',
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
            font-size: 12px;
            color: #fff;
            padding: 16px;
          }
        }
      }
    }
    .info_footer_icon
    {
      display: flex;
      a
      {
        margin: 0 8px;
        padding: 8px;
        background-color: #010101;        
        color: #fff;

      }
    }  
  }
</style>
