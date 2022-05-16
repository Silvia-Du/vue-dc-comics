<template>
  <div class="card">
    <div class="img-box">
      <img :src="cardItem.thumb" :alt="cardItem.type">
    </div>
    <p>{{cardItem.series}}</p>
  </div>
</template>

<script>
export default {
  name: 'CurrSeriescardItem',
  props: {
    cardItem: Object,
  },

  mounted() {
  },
}
</script>

<style lang="scss">

  .card{
    margin: 20px 15px;
    width: 190px;
    text-transform: uppercase;
    .img-box{
      height: 190px;
      overflow: hidden;
      margin-bottom: 15px;
      img{
        width: 100%; 
      }
    }
  }


</style>