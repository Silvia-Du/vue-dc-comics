<template>
  
  <main>
    <div class="jumbotron"></div>

    <div class="current-series">
    <div class="container">
      <CardItem
      v-for="(card, index) in cardSeries" :key="`card-${index}`"
      :cardItem = "card"/>
    </div>
  </div>
    <ShopRow />
  </main>

</template>

<script>

import ShopRow from './ShopRow.vue';
import CardItem from './CardItem.vue';

import cardSeries from '../assets/data/card-series';


export default {
  name : 'MyMain',

  components : {
    ShopRow,
    CardItem
  },

  data(){
    return{
      cardSeries,
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

    .current-series{
    min-height: 100px;
    background-color: #1c1c1c;
    .container{
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      padding: 40px 0;
    }
  }
  }

</style>