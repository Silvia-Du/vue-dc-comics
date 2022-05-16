<template>
  
  <main>
    <div class="jumbotron"></div>

    <div class="current-series">
      <div class="container">
        <div class="flag">
          <p>Current Series</p>
        </div>
        <CardItem
        v-for="(card, index) in cardSeries" :key="`card-${index}`"
        :cardItem = "card"/>
      </div>
      <div class="btn-cta"><p>Load More</p></div>
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

  @import '../assets/style/vars';
  @import '../assets/style/mixin';

  main{
    color: white;
    .jumbotron {
      height: 420px;
      background-image: url(../assets/img/jumbotron.jpg);
      background-size: cover;
      background-position: inherit;
    }

    .current-series {
    min-height: 100px;
    background-color: #1c1c1c;
    text-align: center;
    
    .container {
      display: flex;
      justify-content: center;
      position: relative;
      flex-wrap: wrap;
      padding: 50px 0 40px 0;

      .flag {
      position: absolute;
      top: -26px;
      left: 0;
      padding: 10px 25px;
      color: white;
      font-size: 1.9rem;
      @include textImportant;
      background-color: $brandColor;
      }
    }
    
    .btn-cta {
      display: inline-block;
      padding: 10px 75px;
      margin-bottom: 20px;
      text-transform: uppercase;
      background-color: $brandColor;
    }

  }
  }

</style>