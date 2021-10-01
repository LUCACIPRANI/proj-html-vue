<template>
  <div class="services">
    <img :src="require('../assets/' + info.src)" :alt="info.title" />
    <h1>{{ info.title }}</h1>
    <p>{{ info.description }}</p>
  </div>
</template>

<script>
export default {
  name: "Services",
  props: ["info"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";

.services {
  height: 400px;
  width: 350px;
  margin: 70px 20px;
  padding: 10px;
  img{
    width: 80px;
    height: 140px;
    object-fit: cover;
  }
  img:first-child,
  img:last-child{
    object-fit: contain;
  }
  h1{
    color: $btnColor;
    font-weight: 700;
    margin: 25px 0;
  }
  p{
    @include parag();
    padding: 0 25px;
  }

}
</style>
