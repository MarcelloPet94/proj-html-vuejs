<template>
<div class="strip">
    <h2>{{testo}}</h2>
    <p>{{paragrafo}}</p>
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

.strip
{
    color: #fff;
    text-align: center;
    padding: 32px;
}

</style>
