<template>
  <div class="container">
    <div class="left">
      <img src="../assets/images/shaving_butter.png" alt="">
    </div>
    <div class="right">
      <div class="sm_title"> THIS MONTHS FEATURES PRODUCT</div>
      <div class="title">Shaving Butter</div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores ducimus dolore iure, eos cupiditate officiis adipisci quam, nesciunt veritatis tempora porro cum esse optio deleniti quibusdam nemo totam eum beatae.</p>
      <div class="btn">BUY NOW</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Butter',
  props: ['info'],
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
// @import '~@fortawesome/fontawesome-free/css/all.min.css';
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";

.container{
  background-image: url("../assets/images/avada.jpg");
  background-size: contain;
  background-repeat: no-repeat;
  background-color: $firstTitle;
  height: 60vh;
  width: 80%;
  margin: 0 auto;
  border: 1px solid red;
  @include centerR();
  .left{
    height: 100%;
    width: 40%;
    border: 2px solid green;
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
    padding: 4rem;
    background-color: $footerDown;
    .sm_title{
        font-size: 120%;
        color: $btnColor;
    }
    .title{
        font-size: 500%;
        font-weight: bold;
        color: $mainTitle;
    }
    p{
      line-height: 2rem;
      font-size: 120%;
      color: $secondTitle;
    }
    .btn{
        @include btn();
        width: 30%;
        margin-top: 20px;
        padding: 15px 30px;
        font-size: 110%;
        font-weight: 700;
        background-color: $footerDown;
    }
  }
}
</style>