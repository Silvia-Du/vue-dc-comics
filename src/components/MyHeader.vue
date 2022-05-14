<template>

  <header class=" ">
    <div class="container">

      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <div class="sd-nav">
        <ul>
          <li
          @click="getActiveItem(index)"
          :class="{'active': item.active}"
          v-for="(item, index) in menuItems" :key="`menu-${index}`">
            <a 
            href="item.href">{{item.name}}</a>
          </li>
        </ul>
      </div>
    </div>
  </header>

</template>

<script>
export default {
  name : 'MyHeader',

  data(){
    return{

      clickedItem: -1,

      menuItems: [
        {
          href: '#',
          name: 'CHARACTERS',
          active: true,
        },
        {
          href: '#',
          name: 'COMICS',
          active: false,
        },
        {
          href: '#',
          name: 'MOVIES',
          active: false,
        },
        {
          href: '#',
          name: 'TV',
          active: false,
        },
        {
          href: '#',
          name: 'GAMES',
          active: false,
        },
        {
          href: '#',
          name: 'COLLECTIBLES',
          active: false,
        },
        {
          href: '#',
          name: 'VIDEOS',
          active: false,
        },
        {
          href: '#',
          name: 'FANS',
          active: false,
        },
        {
          href: '#',
          name: 'NEWS',
          active: false,
        },
        {
          href: '#',
          name: 'SHOP',
          active: false,
        }
      ]
    }
  }

}
</script>

<style lang="scss" scoped>

  @import '../assets/style/vars';
  @import '../assets/style/mixin';

  header{
    height: 100px;
    background-color: white;
    display: flex;
    
    .logo img{
      width: 80px;
    }
  }

  .container{
    @include dFlexAlign();
    justify-content: space-between;   
  }

  .sd-nav{
    height: 100%;
    ul{
      height: 100%;
      display: flex;
      list-style: none;
      li{
        &:hover, &.active{
          border-bottom: 3px solid $brandColor; 
          a{
            color: $brandColor;
          }
        }
        height: 100%;
        border-bottom: 3px solid white; 
        @include dFlexAlign;
        a{
          text-decoration: none;  
          color: #494c4f;
          margin: 0 15px;
          font-size: 0.8rem;
          @include textImportant;
        }
      }
    } 
  }

      

 
</style>