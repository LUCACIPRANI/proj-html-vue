<template>
  <div class="award">
    <h1>hsisj</h1>
    <Services :key="index" :info="character"/>
    <Grooming :key="index" :info="character"/>
    <Shaving :key="index" :info="character"/>
    <Reviews :key="index" :info="character"/>
    <Recent :key="index" :info="character"/>

  </div>
</template>

<script>
import Services from './Services.vue'
import Grooming from './Grooming.vue'
import Shaving from './Shaving.vue'
import Reviews from './Reviews.vue'
import Recent from './Recent.vue'

export default {
  name: "Main",
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
  background: black;
  background-image: url("../assets/images/intro-bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
