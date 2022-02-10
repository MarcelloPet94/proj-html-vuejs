<template>
<div class="view_more">
    <p class="stripCta">{{calltoaction}}</p>
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
@import '../../assets/style/variable.scss';
@import '../../assets/style/general.scss';

.view_more
{
    background-color: $mandy;
    text-align: center;
    padding: 42px;
    text-transform: uppercase;
}

</style>
