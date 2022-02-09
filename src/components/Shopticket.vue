<template>
  <section class="ticket_live_date">
    <div class="date_live">
    <Strip 
    :testo="infolive"
    />      
      <ul>
        <li class="show_info_ticket">
          <i class="fas fa-plus"></i><span>17/17</span>
          <div class="hide_show">
            <div class="info_date_live">
              <div class="map_location"></div>
              <div class="shop_ticket">
                <h3>Location</h3>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis autem eaque optio, voluptates, dolor natus et molestiae quo nobis perferendis, similique nihil eligendi at placeat! Rem laborum magnam consectetur tempora?</p>
                <a href="#">Book now</a>
              </div>  
            </div>
          </div>
        </li>     
      </ul>
    </div>
    <Stripaction
    :calltoaction="infolive"
    />  
  </section>
</template>

<script>
import Strip from './partials/Strip.vue'
import Stripaction from './partials/Stripaction.vue'

export default {
  components: {
    Strip,
    Stripaction
  },
  name: 'Savedate',
  props:{
    calltoaction: String
  },
  data() {
    return {
      infolive : "live date"
    }
    
  }
}
</script>

<style scoped lang="scss">

.ticket_live_date
{
  display: flex;
  flex-direction: column;
  column-gap: 200px;
  justify-content: space-between;
  background-color: lightseagreen;
  height: 600px;

  .date_live
  {
    margin: 0 auto;
    width: 800px;

    ul li.show_info_ticket
    { 
      cursor: pointer;      
      padding: 16px;
      list-style-type: none;
      border: 1px solid #fff;

      span 
      {
        margin-left: 16px;
      }

      .hide_show
      {
      display: none;  

        .info_date_live
        {
          display: flex;
          padding-top: 16px;

          .map_location
          {
            min-width: 340px;
            height: 200px;
            margin-right: 16px;
            border: 1px solid #010101;
          }

          .shop_ticket
          {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            
            a
            {
              width: 20%;
              text-align: center;
              line-height: 32px;
              background-color: red;
            }             
          }     
        }
      }   
    }
  }

  ul li.show_info_ticket:hover .hide_show
  {
    display: block;
  }
}

</style>
