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
              <li><a href="#">listItem</a></li>
              <li><a href="#">listItem</a></li>
              <li><a href="#">listItem</a></li>
            </ul>
            <ul>
              <li><p>Title</p></li>
              <li><a href="#">listItem</a></li>
              <li><a href="#">listItem</a></li>
            </ul>
          </div>
          <div class="list debug">
            <ul>
              <li><p>Title</p></li>
              <li><a href="#">listItem</a></li>
              <li><a href="#">listItem</a></li>
              <li><a href="#">listItem</a></li>
              <li><a href="#">listItem</a></li>
            </ul>
          </div>
          <div class="list debug">
            <ul>
              <li><p>Title</p></li>
              <li><a href="#">listItem</a></li>
              <li><a href="#">listItem</a></li>
              <li><a href="#">listItem</a></li>
              <li><a href="#">listItem</a></li>
            </ul>
          </div>
        </div>
        <img src="../assets/img/dc-logo-bg.png" alt="logo-bg">

      </div>
    </div>
    <!-- bottom -->
    <div class="bottom">
      <div class="container">B</div>
    </div>
      
    
    
  </footer>

</template>

<script>
export default {
  name : 'MyFooter'
}
</script>

<style lang="scss" scoped>

  @import '../assets/style/mixin';


  footer{
     min-height: 200px;
    .top{
      height: 350px;
      overflow: hidden;
      background-image: url(../assets/img/footer-bg.jpg);
      @include backGround();
    }
    .bottom{
      height: 100px;
      background-color: #303030;
    }
  }

  .top .container{
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
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
        }
        a{
          text-decoration: none;
          font-size: 0.8rem;
          color: rgb(209, 203, 203);
          margin: 10px 0;
        }
      }
    }
    
  }




</style>