<template>
  <section class="main">
    <Stripseo
    :testo="tNews"
    :paragrafo="paragrafoNews"
    />
    <div class="grid_news">
        <div class="sx_block">
            <div class="news_thumb" :class="see.alignState" v-for="see in news" :key="see.id">
              <img class="img_cont" :src="see.media" alt="">              
              <div class="thumb_onhover">
                <p class="paragraphHoverNews">{{see.titNews}}</p>
                </div>
              <div class="content_thumb">
                <p class="titleNews">{{see.titNews}}</p>
                <p class="parNews">{{see.titPar}}</p>
              </div>
            </div>
        </div>
        <div class="dx_block">
            <div class="news_thumb" :class="dx.alignState" v-for="dx in newsDx" :key="dx.id">
              <img class="img_cont" :src="dx.media" alt="">
              <div class="thumb_onhover"><p class="paragraphHoverNews">{{dx.titNews}}</p></div>              
              <div class="content_thumb">
                <p class="titleNews">{{dx.titNews}}</p>
                <p class="parNews">{{dx.titPar}}</p>
              </div>              
            </div>
        </div>
    </div>
    <Stripaction
    :calltoaction="cta"
    />  
  </section>
  
</template>

<script>
import Stripseo from './partials/Stripseo.vue'
import Stripaction from './partials/Stripaction.vue'
import dataNews from '../pageData/news.js'
import newsDx from '../pageData/newsDx.js'

export default {
  name: 'Main',
  components: {
    Stripseo,
    Stripaction
  },
  data(){
    return{
      tNews : "Latest Band News",
      paragrafoNews: "lorem",
      cta : "view all latest news",
      news: dataNews,
      newsDx: newsDx
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/style/variable.scss';

.main
{
  background-color: $charade;

  .grid_news{
    display: flex;
    justify-content: space-between;
    margin: 0 auto;
    width: 800px;
    height: auto;
    margin-bottom: 80px;

    .news_thumb
    {
      position: relative;
      overflow: hidden;

      .img_cont
      {
        position: absolute;
        top: 0;
        width: 113%;
      }

      .thumb_onhover
      {
        display: none;
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: rgba(235 , 75 , 93 , 0.8);
        z-index: 1;

        p
        {
          position: relative;
          top: 50%;
          text-align: center;
        }
      }

      .content_thumb
      {
        position: absolute;
        bottom: 0;
        width: 100%;
        padding: 16px;
        background-color: #323844;
        color: #fff;
      }
    }

    .sx_block
    {
      display: grid;
      grid-gap: 16px;
      width: calc(68% - 16px);
      height: 100%;

      .box1
      {
        grid-column: 1 /span 2;
        height: 184px;
      }

      .box2, .box3
      {
        height: 416px;
      }

      .box4
      {
        grid-column: 1 /span 2;
        height: 184px;
      }

    }

    .dx_block
    {
      display: grid;;
      grid-gap: 16px;      
      width: 32%;
      height: 100%;

      .box_dx1
      {
        height: 400px;
      }
      
      .box_dx2
      {
        height: 400px;
      }
    }
  }

  .grid_news .news_thumb:hover .thumb_onhover  
    {
      display: block;

    }

  .grid_news .news_thumb:hover .content_thumb
    {
      display: none;
    }  
}

</style>
