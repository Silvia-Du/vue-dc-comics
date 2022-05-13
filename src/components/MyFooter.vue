<template>
  
  <footer class="debug">
    <!-- top -->
    <div class="top">

      <div class="container">

        <div class="list-container">
          <div class="list debug">
            <ul
            v-for="(item, index) in lists[0]" :key="`list-${index}`">
              <li><p>{{item.title}}</p></li>
              <li><a href="#">{{}}</a></li>

            </ul>
            <ul>
              <li><p>Title</p></li>
              <li><a href="#">listItem</a></li>
            </ul>
          </div>
          <div class="list debug">
            <ul>
              <li><p>Title</p></li>
              <li><a href="#">listItem</a></li>
            </ul>
          </div>
          <div class="list debug">
            <ul>
              <li><p>Title</p></li>
              <li><a href="#">listItem</a></li>
            </ul>
          </div>
        </div>
        <img src="../assets/img/dc-logo-bg.png" alt="logo-bg">

      </div>
    </div>
    <!-- bottom -->
    <div class="bottom">
      <div class="container cta">
        <div class="button">
          <p>sign-up-now!</p>
        </div>
        <div class="cta-social">
          <p>Follow us</p>
          <div 
          v-for="(icon, index) in icons" :key="`icons-${index}`"
          class="icon-circle">
            <i :class="`fa-${icon.prefix} fa-${icon.name}`"></i>
          </div>
        </div>
      </div>
    </div>
      
    
    
  </footer>

</template>

<script>
export default {
  name : 'MyFooter',

  data(){
    return{
      icons:[
        {
          name:'facebook-f',
          prefix: 'brands'
        },
        {
          name:'twitter',
          prefix: 'brands'
        },
        {
          name:'youtube',
          prefix: 'brands'
        },
        {
          name:'pinterest-p',
          prefix: 'brands'
        },
        {
          name:'location-dot',
          prefix: 'solid'
        },
      ],

      lists:[
        {
          title: 'dc comics',
          items: [
            'Characters', 'comics', 'movies', 'TV', 'games', 'Videos', 'news'
          ]
        },
        {
          title: 'shop',
          items: [
            'shop DC', 'Shop DC Collectibles'
          ]
        },
        {
          title: 'dc',
          items: [
            'therms Of Use', 'Privacy policy (New)', 'Ad choice', 'advertising', 'jobs', 'Subscriptions', 'talent Workshop', 'CPSC Certficates', 'ratings', 'shop Help', 'contact Us'
          ]
        },
        {
          title: 'dc',
          items: [
            'DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Powe Visa'
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

  @import '../assets/style/vars';
  @import '../assets/style/mixin';


  footer{
    .top{
      height: 400px;
      overflow: hidden;
      background-image: url(../assets/img/footer-bg.jpg);
      @include backGround();
    }
    .bottom{
      height: 90px;
      background-color: #303030;
    }
  }
  //FOOTER TOP
  .top .container{
    height: 100%;
    @include dFlexBetween();
    img{
      width: 60%;
    }
  }

  .list-container{
    color: white;
    font-size: 1rem;
    display: flex;
    align-self: flex-start;
    margin-top: 30px;
    .list{
      margin: 0 20px;
      ul li{
        list-style: none;
        p{
          margin: 15px 0;
          font-weight: bold;
          font-size: 0.9rem;
        }
        a{
          text-decoration: none;
          font-size: $mainfontSize;
          color: rgb(209, 203, 203);
          margin: 10px 0;
        }
      }
    } 
  }

  // FOOTER BOTTOM

  .bottom .container{
    height: 100%;
    @include dFlexBetween;
    .button{
      display: inline-block;
      border: 2px solid $brandColor;
      color: white;
      @include textImportant;
      font-size: $mainfontSize;
      padding: 10px 15px;
    }
    .cta-social{
      @include dFlexAlign;
      p{
        font-size: 0.9rem;
        @include textImportant;
        color: $brandColor;
      }
      .icon-circle{
        @include dFlexAlign;
        justify-content: center;
        width: 30px;
        height: 30px;
        font-size: 1.4rem;
        border-radius: 50%;
        margin-left: 10px;
        color: #303030;
        background-color: #797979;
      }
    }
  }




</style>