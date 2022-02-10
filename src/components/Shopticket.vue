<template>
  <section class="ticket_live_date" id="livedate">
    <div class="date_live">
    <Stripseo 
    :testo="dNews"
    :paragrafo="paragrafoData"
    />    
        <ul v-for="info  in dataticket" :key="info.id">
          <li class="show_info_ticket">
            <div>
              <i class="fas fa-plus"></i>
              <i class="fas fa-minus"></i>
              <span>{{info.date}} {{info.location}}</span>
            </div>
            <div class="hide_show">
              <div class="info_date_live">
                <div class="map_location"></div>
                <div class="shop_ticket">
                  <h3>{{info.title}}</h3>
                  <p>{{info.more}}</p>
                  <a href="#">{{info.cta}}</a>
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
import Stripseo from './partials/Stripseo.vue'
import Stripaction from './partials/Stripaction.vue'
import allTicket from '../pageData/ticket.js'

export default {
  components: {
    Stripseo,
    Stripaction
  },
  name: 'Savedate',
  props:{
    calltoaction: String
  },
  data() {
    return {
      dNews : "Live Dates",
      paragrafoData : "lorem",  
      infolive : "View all live dates",
      dataticket: allTicket      
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

      .hide_show , .fa-minus
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
              width: 100px;
              text-align: center;
              line-height: 32px;
              background-color: red;
            }             
          }     
        }
      }   
    }
  }

  ul li.show_info_ticket:hover .hide_show , ul li.show_info_ticket:hover .fa-minus
  {
    display: inline-block;
  }

  ul li.show_info_ticket:hover .fa-plus
  {
    display: none;
  }

}

</style>
