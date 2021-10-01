<template>
<header>
  <div class="container">
    <div class="nav-top">
      <div class="logo">
        <img class="ct-img" src="../assets/images/logo.png" alt="" />
      </div>
      <div class="menu">
        <i class="fas fa-shopping-cart"></i>
        <i class="fas fa-bars"></i>
      </div>
    </div>
    <div class="homePage">
      <div class="left">
        <h1>Barber Shop</h1>
        <div class="content">
          <div class="line"></div>
          <p>The Pinnacle of Male Grooming</p>
          <div class="btn">LEARN MORE</div>
        </div>
      </div>
      <div class="right">
        <img src="../assets/images/homepage_first.png" alt="Cutting hair picture">
        <i class="fas fa-window-restore"> <span>Demos</span></i>
        <i class="fas fa-shopping-cart"><span>Buy Now</span></i>
      </div>
    </div>
  </div>

</header>
</template>

<script>
export default {
  name: 'Header',
  props: ['msg']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";

header{
  height: 95vh;
  width: 100%;
  background-image: url("../assets/images/bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
.container{
  width: 100%;
  margin: 0 auto;
}
.nav-top{
  padding-top: 30px;
  @include centerR();
  .logo{
    width: 58%;
  }
}
.menu .fas{
  margin: 0 10px;
}
.fa-shopping-cart{
color: $firstTitle;
}
.fa-bars{
  font-size: 170%;
  color: $btnColor;
}
.homePage{
  @include centerR();
  margin: 0 auto;
  width: 100%;
  .left{
    position: relative;
    @include centerC();
    width: 60%;
    h1{
      @include title();
      position: absolute;
      bottom: 100px;
    }
    .content{
      position: absolute;
      top: -120px;
      left: 20%;
      .line{
        border-bottom: 4px solid $btnColor;
        height: 60px;
        width: 240px;
        margin-bottom: 2rem;
      }
      p{
        font-size: 160%;
        color: $secondTitle;
        margin-bottom: 2rem;
      }
      .btn{
        @include btn();
        padding: 17px 3px;
        width: 60%;
        font-weight: bold;
      }
    }
  }
  .right{
    position: relative;
    img{
      width: 70%;
    }
    .fa-window-restore,
    .fa-shopping-cart{
      position: absolute;
      top: 8%;
      right: 1%;
      @include centerC();
      background-color: white;
      border-radius: 8px;
      margin: 5px 0;
      height: 65px;
      width: 65px;
      font-size: 140%;
        color: #33475B;
      span{
        font-size: 65%;
        padding-top: 5px;
      }
    }
    .fa-shopping-cart{
      position: absolute;
      top: 19%;
    }
  }
}
</style>
