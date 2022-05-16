<template>
  <div class="current-series">
    <div class="container debug">
      <div class="card">
        <img src="" alt="">
        <p>titolo fumetto</p>
      </div>
    </div>
  </div>
</template>

<script>

import cardSeries from '../assets/data/card-series';



export default {
  name: 'CurrentSeries',

  data(){
    return{
      cardSeries,
    }
  },

  mounted() {
    console.log(cardSeries);
  },
}
</script>

<style lang="scss">

  .current-series{
    min-height: 100px;
    background-color: #1c1c1c;
  }

</style>