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
    <Shaving/>
    <Reviews/>
    <Recent/>
</main>

</template>

<script>
import * as servicesD from "@/datas/services.js";

import Services from './Services.vue'
import Grooming from './Grooming.vue'
import Shaving from './Shaving.vue'
import Reviews from './Reviews.vue'
import Recent from './Recent.vue'

export default {
  name: "Main",
  data() {
      return{
          services: servicesD,
      }
  },
  props: {},
  components: {
      Services,
      Grooming,
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
  background-image: url("../assets/images/intro-bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  @include centerC();
  .sm_title{
      @include sm-title();
  }
  .title{
      @include title();
  }
  .btn{
      @include btn();
      width: 20%;
      padding: 18px;
  }
}
</style>
