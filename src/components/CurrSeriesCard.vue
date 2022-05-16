<template>
  <div class="card">
    <img :src="cardItem.thumb" :alt="cardItem.type">
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
    width: calc((100% / 6) - 25px);
    img{
      width: 100%;
      height: ;

    }
  }


</style>