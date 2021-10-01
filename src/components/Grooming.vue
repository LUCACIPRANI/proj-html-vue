<template>
  <div class="container">
    <div class="sm_title"> WE HAVE YOU COVERED</div>
    <div class="title">Avada Grooming Products</div>
    <div>

    </div>
    <div class="btn">SHOP OUR PRODUCT RANGE</div>
  </div>
</template>

<script>
// import
export default {
  name: 'Grooming',
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
  height: 120vh;
  background-image: url("../assets/images/avadabarbers-reviewsbackground.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  @include startCol();
  .sm_title{
      @include sm-title();
  }
  .title{
      @include title();
  }
  .btn{
      @include btn();
      width: 25%;
      padding: 18px;
  }
}

</style>