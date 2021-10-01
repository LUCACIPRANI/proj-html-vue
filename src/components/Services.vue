<template>
  <div class="container">
    <div class="award">
        <div class="sm_title"> MENS GROOMING</div>
        <div class="title">Services</div>
        <div class="services">
          <h1>{{info.title}}</h1>
        </div>
        <div class="btn">READ ABOUT OUR SERVICES</div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Services',
  props: ['info']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";

.container{
  background-color: $firstTitle;
  height: 120vh;
  border: 1px solid red;
  @include startCol();
  .sm_title{
      font-size: 120%;
      color: $btnColor;
  }
  .title{
      font-size: 500%;
      font-weight: bold;
      color: $mainTitle;
  }
  .btn{
      @include btn();
      margin-top: 20px;
      padding: 15px 30px;
      font-size: 110%;
      font-weight: 700;
      background-color: $firstTitle;
  }
  .services{
    height: 500px;
    border: 1px solid red;
  }
}
</style>