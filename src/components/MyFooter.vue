<template>
  
  <footer class="debug">
    <!-- top -->
    <div class="top">

      <div class="container">
        <div class="list-container">
          <div class="list debug">
            <ul>
              <li><p>Title</p></li>
              <li><a href="#">listItem</a></li>

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
          <div class="icon-circle">
            <i class="fa-brands fa-facebook-f"></i>
          </div>
        </div>
      </div>
    </div>
      
    
    
  </footer>

</template>

<script>
export default {
  name : 'MyFooter'
}
</script>

<style lang="scss" scoped>

  @import '../assets/style/vars';
  @import '../assets/style/mixin';


  footer{
    .top{
      height: 350px;
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
    @include dFlexAlign();
    justify-content: space-between;
    img{
      width: 450px;
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
    @include dFlexAlign();
    justify-content: space-between;
    .button{
      display: inline-block;
      border: 2px solid $brandColor;
      color: white;
      font-weight: bold;
      text-transform: uppercase;
      font-size: $mainfontSize;
      padding: 10px 15px;
    }
    .cta-social{
      @include dFlexAlign;
      p{
        font-size: 0.9rem;
        font-weight: bold;
        color: $brandColor;
        text-transform: uppercase;
      }
      .icon-circle{
        @include dFlexAlign;
        justify-content: center;
        width: 30px;
        height: 30px;
        border-radius: 50%;
        margin-left: 10px;
        color: #303030;
        background-color: #797979;
      }
    }
  }




</style>