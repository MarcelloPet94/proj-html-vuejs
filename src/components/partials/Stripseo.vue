<template>
<div class="strip">
    <h2 class="standardText">{{testo}}</h2>
    <div class="definition_line"></div>
    <p class="standarParagraph">{{paragrafo}}</p>
</div>
</template>

<script>

export default {
  name: 'App',
  props:{
      testo : String,
      paragrafo: String
  }
}
</script>

<style lang="scss">
@import '../../assets/style/variable.scss';
@import '../../assets/style/general.scss';

.strip
{
    color: #fff;
    text-align: center;
    padding: 32px;

    .definition_line
    {
        position: relative;
        left: 37%;
        border: 1px solid $bombay;
        opacity: 0.2;
        margin: 16px 0;
        width: calc(100% - 75%);
    }
}

</style>
