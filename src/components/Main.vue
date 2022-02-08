<template>
  <section class="main">
    <Strip
    :testo="prova2"
    />
    <div class="grid_news">
        <div class="sx_block">
            <div class="news_thumb box1">
              <div class="content_thumb">
                argomento
              </div>
            </div>
            <div class="news_thumb box2">
              <div class="content_thumb">
                argomento
              </div>
            </div>
            <div class="news_thumb box3">
              <div class="content_thumb">
                argomento
              </div>
            </div>
            <div class="news_thumb box4">
              <div class="content_thumb">
                argomento
              </div>
            </div>
        </div>
        <div class="dx_block">
            <div class="news_thumb box_dx1">
              <div class="content_thumb">
                argomento
              </div>              
            </div>
            <div class="news_thumb box_dx2">
              <div class="content_thumb">
                argomento
              </div>              
            </div>
        </div>
    </div>
  </section>
  
</template>

<script>
import Strip from './partials/strip.vue'

export default {
  name: 'Main',
  components: {
    Strip
  },
  data(){
    return{
      prova2 : "direttamente da main"
    }
  }
}
</script>

<style scoped lang="scss">

.main
{
  padding: 80px;
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
}

</style>
