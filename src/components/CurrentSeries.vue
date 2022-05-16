<template>
  <div class="current-series">
    <div class="container debug">
      <CurrSeriesCard 
      v-for="(card, index) in cardSeries" :key="`card-${index}`"
      :cardItem = "card"/>
    </div>
  </div>
</template>

<script>

import cardSeries from '../assets/data/card-series';
import CurrSeriesCard from './CurrSeriesCard.vue';



export default {
    name: "CurrentSeries",
    data() {
        return {
            cardSeries,
        };
    },
    mounted() {
        // console.log(cardSeries);
    },
    components: { CurrSeriesCard }
}
</script>

<style lang="scss">

  .current-series{
    min-height: 100px;
    background-color: #1c1c1c;
    .container{
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
      padding: 40px 0;
    }
  }

</style>