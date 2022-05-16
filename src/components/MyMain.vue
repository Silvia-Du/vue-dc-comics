<template>
  
  <main>
    <div class="jumbotron"></div>
    <CurrentSeries />
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
  },

  data(){
    return{
    }
  },

}
</script>

<style lang="scss">

  main{
    color: white;
    .jumbotron{
      height: 420px;
      background-image: url(../assets/img/jumbotron.jpg);
      background-size: cover;
      background-position: inherit;
    }
  }

</style>