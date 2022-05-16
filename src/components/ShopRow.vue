<template>
  <div class="shop-row">
    <div class="container">

      <div 
      v-for="(item, index) in ctaShopItems" :key="`ctaItem-${index}`"
      class="item">
        <a :href="item.href"><img :src="item.image" :alt="item.name"></a>       
        <p>{{item.name}}</p>
      </div>
      
    </div>
  </div>
</template>

<script>

export default {
  name: 'ShopRow',

  data(){
    return{


      ctaShopItems : [
        {
          name : 'digital comics',
          image : require('../assets/img/buy-comics-digital-comics.png'),
          href : '#'
        },
        {
          name : 'dc merchandise',
          image : require('../assets/img/buy-comics-merchandise.png'),
          href : '#'
        },
        {
          name : 'subscription',
          image : require('../assets/img/buy-comics-subscriptions.png'),
          href : '#'
        },
        {
          name : 'comic shop locator',
          image : require('../assets/img/buy-comics-shop-locator.png'),
          href : '#'
        },
        {
          name : 'dc power visa',
          image : require('../assets/img/buy-dc-power-visa.svg'),
          href : '#'
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

  @import '../assets/style/vars';
  @import '../assets/style/mixin';

  .shop-row{
    color: white;
    background-color: #0282f9;
    .container{
      padding: 40px;
      display: flex;
      justify-content: space-between;
    }
  }

  .item{
    @include dFlexAlign;
    &:last-child{
        img{
          height: auto;
          width: 70px;
        }
      }
    img{
      height: 60px;
    }

    p{
      font-size: $mainfontSize;
      margin-left: 25px;
      text-transform: uppercase;
    }
  }
</style>