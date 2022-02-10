<template>
  <section class="main">
    <Stripseo
    :testo="tNews"
    :paragrafo="paragrafoNews"
    />
    <div class="grid_news">
        <div class="sx_block">
            <div class="news_thumb" :class="see.alignState" v-for="see in news" :key="see.id">
              <div class="thumb_onhover">
                <p>{{see.titNews}}</p>
                </div>
              <div class="content_thumb">
                <p>{{see.titNews}}</p>
                <p>{{see.titPar}}</p>
              </div>
            </div>
        </div>
        <div class="dx_block">
            <div class="news_thumb" :class="dx.alignState" v-for="dx in newsDx" :key="dx.id">
              <img class="img_cont" :src="dx.media" alt="">
              <div class="thumb_onhover"><p>{{dx.titNews}}</p></div>              
              <div class="content_thumb">
                <p>{{dx.titNews}}</p>
                <p>{{dx.titPar}}</p>
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

.main
{
  background-color: lightblue;

  .grid_news{
    display: flex;
    justify-content: space-between;
    margin: 0 auto;
    width: 800px;
    height: auto;
    border: 4px solid yellow;

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
        background-color: rgba(237, 57, 21, 0.8);
        border: 5px solid #010101;
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
        background-color: darkblue;
        color: #fff;
      }
    }

    .sx_block
    {
      display: grid;
      grid-gap: 16px;
      width: calc(70% - 16px);
      height: 100%;
      border: 1px solid #010101;

      .box1
      {
        grid-column: 1 /span 2;
        height: 184px;
        background-color: lightgreen;
      }

      .box2, .box3
      {
        background-color: yellow;
        height: 416px;
      }

      .box4
      {
        grid-column: 1 /span 2;
        background-color: orange;
        height: 184px;
      }

    }

    .dx_block
    {
      display: grid;;
      grid-gap: 16px;      
      width: 30%;
      height: 100%;
      border: 1px solid #010101;

      .box_dx1
      {
        background-color: lightsalmon;
        height: 400px;
      }
      
      .box_dx2
      {
        background-color: lightsalmon;        
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
