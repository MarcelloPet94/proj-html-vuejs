<template>
  <section class="main">
    <Strip
    :testo="prova2"
    />
    <div class="grid_news">
        <div class="sx_block">
            <div class="news_sx box1">1</div>
            <div class="news_sx box2">2</div>
            <div class="news_sx box3">3</div>
            <div class="news_sx box4">4</div>
        </div>
        <div class="dx_block">
            <div class="news_sx box_dx1">1</div>
            <div class="news_sx box_dx2">2</div>
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
