<template>

  <header class=" ">
    <div class="container">

      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <div class="sd-nav">
        <ul class="mb-0">
          <li><a href="#">characters</a></li>
          <li><a href="#">comics</a></li>
          <li><a href="#">movies</a></li>
          <li><a href="#">tv</a></li>
          <li><a href="#">games</a></li>
          <li><a href="#">navItem</a></li>
          <li><a href="#">navItem</a></li>
          <li><a href="#">navItem</a></li>
          <li><a href="#">navItem</a></li>
          <li><a href="#">navItem</a></li>
        </ul>
      </div>
    </div>
  </header>

</template>

<script>
export default {
  name : 'MyHeader'
}
</script>

<style lang="scss" scoped>

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
      ul{
        display: flex;
        list-style: none;
         li a{
          text-decoration: none;  
          color: #494c4f;
          margin: 0 15px;
          text-transform: uppercase;
          font-size: 0.7rem;
        }
      } 
    }

 
</style>