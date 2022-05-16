<template>
  
  <main>
    <div class="jumbotron"></div>
    <div class="container">
      <CurrentSeries />
    </div>
    <ShopRow />
  </main>

</template>

<script>

import ShopRow from './ShopRow.vue';
import CurrentSeries from './CurrentSeries.vue';

export default {
  name : 'MyMain',

  components : {
    ShopRow,
    CurrentSeries
}
}
</script>

<style lang="scss">

  main{
    color: white;
    background-color: #1c1c1c;
    .jumbotron{
      height: 25vh;
      background-image: url(../assets/img/jumbotron.jpg);
      background-size: cover;
      background-position: inherit;
    }
    .container{
      padding: 50px 0;
    }
  }

</style>