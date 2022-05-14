<template>
  
  <footer class="debug">
    <!-- top -->
    <div class="top">

      <div class="container">

        <div class="list-container">
          <div class="list">
            <p>Dc Comics</p>
            <ul
            v-for="(item, index) in dcComicsList" :key="`dcList-${index}`">
              <li><a :href="item.href">{{item.name}}</a></li>

            </ul>
            <p>Shop</p>
            <ul
            v-for="(item, index) in shopList" :key="`shopL-${index}`">
              <li><a :href="item.href">{{item.name}}</a></li>
            </ul>
          </div>
          <div class="list">
            <p>Dc</p>
            <ul
            v-for="(item, index) in dcList" :key="`dcList-${index}`">
              <li><a :href="item.href">{{item.name}}</a></li>
            </ul>
          </div>
          <div class="list">
            <p>Sites</p>
            <ul
            v-for="(item, index) in sitesList" :key="`sitesL-${index}`">
              <li><a :href="item.href">{{item.name}}</a></li>
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

      dcComicsList:[
        {
          name: 'Characters',
          href: '#'
        },
        {
          name: 'comics',
          href: '#'
        },
        {
          name: 'movies',
          href: '#'
        },
        {
          name: 'TV',
          href: '#'
        },
        {
          name: 'games',
          href: '#'
        },
        {
          name: 'videos',
          href: '#'
        },
        {
          name: 'news',
          href: '#'
        }
      ],

      shopList:[
         {
          name: 'shop DC',
          href: '#'
        },
         {
          name: 'Shop DC Collectibles',
          href: '#'
        }
      ],

      dcList:[
        {
          name: 'therms Of Use',
          href: '#'
        },
        {
          name: 'Privacy policy (New)',
          href: '#'
        },
        {
          name: 'ad choice',
          href: '#'
        },
        {
          name: 'advertising',
          href: '#'
        },
        {
          name: 'jobs',
          href: '#'
        },
        {
          name: 'Subscriptions',
          href: '#'
        },
        {
          name: 'talent Workshop',
          href: '#'
        },
        {
          name: 'CPSC Certficates',
          href: '#'
        },
        {
          name: 'ratings',
          href: '#'
        },
        {
          name: 'shop Help',
          href: '#'
        },
        {
          name: 'contact Us',
          href: '#'
        },
      ],

      sitesList:[
        {
          name : 'DC',
          href : '#'
        },
        {
          name : 'MAD Magazine',
          href : '#'
        },
        {
          name : 'DC Kids',
          href : '#'
        },
        {
          name : 'DC Universe',
          href : '#'
        },
        {
          name : 'DC Powe Visa',
          href : '#'
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
      p{
        margin: 10px 0;
        font-weight: bold;
        font-size: 1rem;
        text-transform: uppercase;
      }
      ul li{
        list-style: none;
        a{
          text-decoration: none;
          font-size: $mainfontSize;
          color: rgb(117, 111, 111);
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
      font-size: 0.9rem;
      @include textImportant;
      padding: 10px 15px;
    }
    .cta-social{
      @include dFlexAlign;
      p{
        font-size: 1.1rem;
        margin-right: 20px;
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