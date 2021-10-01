<template>
  <div class="container">
    <div class="sm_title"> TALES FROM THE BARBER SHOP</div>
    <div class="title">Recent Blog posts</div>
    <div></div>
    <div class="btn">READ MORE FROM OUR BLOG</div>
  </div>
</template>

<script>
export default {
  name: 'Recent',
  props: ['msg']
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
  background-color: #F5F5F5;
  @include startCol();
  .sm_title{
      @include sm-title();
  }
  .title{
      @include title();
  }
  .btn{
    @include btn();
    padding: 18px 20px;
    background-color: #F5F5F5;
  }
}
</style>