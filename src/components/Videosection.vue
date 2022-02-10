<template>
  <div class="video_section">
    <img src="" alt="">
    <div class="content_text_video">
    <p class="emotionalText">Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores eum assumenda officiis eaque? Obcaecati,
      ipsa ut quae pariatur ea cumque maiores ab. Molestias natus veritatis optio asperiores,
      a inventore necessitatibus.</p>
    </div>  
    <div class="play_button">
      <img src="../assets/band_interview_play_icon.png" alt="play">
    </div>  
  </div>
</template>

<script>
export default {
  name: 'Videosection',
}
</script>

<style scoped lang="scss">
.video_section
{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 700px;
  background-image: url(../assets/home-testimonial-parallax.jpg);
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;  

  .content_text_video
  {
    width: 50%;
    text-align: center;
    color: #fff;
  }

  .play_button
  {
    width: 60px;
    margin: 24px;

    img
    {
      width: 100%;
    }
  }
}
</style>
