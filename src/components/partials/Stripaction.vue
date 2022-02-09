<template>
<div class="view_more">
    <h1>{{calltoaction}}</h1>
</div>
</template>

<script>

export default {
  name: 'App',
  props:{
      calltoaction : String
  }
}
</script>

<style lang="scss">

.view_more
{
    background-color: red;
    text-align: center;
    padding: 32px;
}

</style>
