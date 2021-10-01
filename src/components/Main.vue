<template>
<main>
    <div class="award">
        <div class="sm_title"> AWARD WINNING</div>
        <div class="title">Pro Barbers</div>
        <div class="btn">MEET YOUR NEW BARBER</div>
    </div>
    <Services 
        v-for="(service, index) in services" 
        :key="index"
        :info="service"
    />
    <Grooming/>
    <Butter/>
    <Shaving/>
    <Reviews/>
    <Recent/>
</main>

</template>

<script>
// import services from "@/src/datas/services.js";

import Services from './Services.vue'
import Grooming from './Grooming.vue'
import Butter from './Butter.vue'
import Shaving from './Shaving.vue'
import Reviews from './Reviews.vue'
import Recent from './Recent.vue'

export default {
  name: "Main",
  props: {},
  components: {
      Services,
      Grooming,
      Butter,
      Shaving,
      Reviews,
      Recent,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";

.award {
  height: 60vh;
  background: black;
  background-image: url("../assets/images/intro-bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  @include centerC();
  .sm_title{
      font-size: 120%;
      color: $btnColor;
  }
  .title{
      font-size: 500%;
      color: $mainTitle;
  }
  .btn{
      @include btn();
      margin-top: 20px;
      width: 20%;
      padding: 18px;
      font-size: 110%;
      font-weight: 600;
  }
}
</style>
