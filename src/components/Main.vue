<template>
  <section class="main">
    <Strip
    :testo="prova2"
    />
    <div class="grid_news">
        <div class="sx_block">
            <div class="news_thumb box1">
              <div class="thumb_onhover"><p>argomento</p></div>
              <div class="content_thumb">
                <p>argomento</p>
              </div>
            </div>
            <div class="news_thumb box2">
              <div class="thumb_onhover"><p>argomento</p></div>           
              <div class="content_thumb">
                argomento
              </div>
            </div>
            <div class="news_thumb box3">
              <div class="thumb_onhover"><p>argomento</p></div>              
              <div class="content_thumb">
                argomento
              </div>
            </div>
            <div class="news_thumb box4">
              <div class="thumb_onhover"><p>argomento</p></div>              
              <div class="content_thumb">
                argomento
              </div>
            </div>
        </div>
        <div class="dx_block">
            <div class="news_thumb box_dx1">
              <div class="thumb_onhover"><p>argomento</p></div>              
              <div class="content_thumb">
                argomento
              </div>              
            </div>
            <div class="news_thumb box_dx2">
              <div class="thumb_onhover"><p>argomento</p></div>              
              <div class="content_thumb">
                argomento
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
import Strip from './partials/Strip.vue'
import Stripaction from './partials/Stripaction.vue'

export default {
  name: 'Main',
  components: {
    Strip,
    Stripaction
  },
  data(){
    return{
      prova2 : "direttamente da main",
      cta : "call to action"
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
    width: 900px;
    height: auto;
    border: 4px solid yellow;

    .news_thumb
    {
      position: relative;

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
        height: 90px;
        padding: 8px;
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
