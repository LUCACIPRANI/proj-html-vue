<template>
  <div class="container">
    <div class="award">
        <div class="sm_title"> MENS GROOMING</div>
        <div class="title">Services</div>
        <div class="products">
          <div class="services">
            <img :src="require(info.src)" :alt="info.title">
            <h5>{{info.title}}</h5>
            <p>{{info.description}}</p>
          </div>
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
  height: 135vh;
  @include startCol();
  .sm_title{
      @include sm-title();
  }
  .title{
      @include title();
  }
  p{
     @include parag();
  }
  .btn{
    @include btn();
    padding: 18px 20px;
    margin-left: 40px; //momentaneo
    width: 80%;
    background-color: $firstTitle;
  }
  .products{
    @include centerR();
    .services{
      height: 400px;
      width: 350px;
      border: 1px solid red;  //debug
      margin: 70px 20px;
    }
  }
}
</style>