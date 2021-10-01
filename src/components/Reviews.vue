<template>
<div class="main-container">
  <div class="container-top">
    <div class="left">
      <img src="../assets/images/shaving_butter.png" alt="">
    </div>
    <div class="right">
      <div class="sm_title"> THIS MONTHS FEATURES PRODUCT</div>
      <div class="title">Shaving Butter</div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores ducimus dolore iure, eos cupiditate officiis adipisci quam, nesciunt veritatis tempora porro cum esse.</p>
      <div class="btn">BUY NOW</div>
    </div>
  </div>
  <div class="container-review">
    <div class="reviews">
      <div class="sm_title"> WHAT PEOPLE SAY</div>
      <div class="title">Reviews</div>
      <div class="column">

      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Reviews',
  props: ['msg']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";
.main-container{
  height: 180vh;
  position: relative;
}
.container-top{
  position: absolute;
  top: -40px;
  left: 10%;
  background-image: url("../assets/images/avada.jpg");
  background-size: contain;
  background-repeat: no-repeat;
  background-color: $firstTitle;
  border-top: 4px solid $btnColor;
  height: 33%;
  width: 80%;
  margin: 0 auto;
  @include centerR();
  .left{
    height: 100%;
    width: 40%;
    @include centerR();
    img{
      object-fit: contain;
      height: 400px;
      width: 400px;
    }
  }
  .right{
    width: 60%;
    height: 100%;
    padding: 5rem;
    background-color: $footerDown;
    .sm_title{
        @include sm-title();
    }
    .title{
        @include title();
        padding-bottom: 15px;
    }
    p{
       @include parag();
    }
    .btn{
        @include btn();
        width: 30%;
        padding: 15px 30px;
        background-color: $footerDown;
    }
  }
}
.container-review{
  position: relative;
  .reviews{
    position: absolute;
    top: 850px;
    left: 50%;
    transform: translate(-50%, -50%);
  }
  .sm_title{
    text-align: center;
    @include sm-title();
  }
  .title{
      @include title();
  }
  .column{
    height: 400px;
    margin-top: 100px;
    border: 2px solid green;
  }
}
</style>