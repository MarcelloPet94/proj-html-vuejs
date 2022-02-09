<template>
<div class="strip">
    <h1>{{testo}}</h1>
</div>
</template>

<script>

export default {
  name: 'App',
  props:{
      testo : String
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
