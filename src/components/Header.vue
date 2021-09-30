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
    <div class="description">
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
  height: 100vh;
  width: 100%;
  background-image: url("../assets/images/bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
.container{
  width: 100%;
  margin: 0 auto;
  color: white;
}
.nav-top{
  padding-top: 20px;
  @include centerR();
}
.menu .fas{
  margin: 0 10px;
}
.fa-bars{
  font-size: 170%;
}
</style>
