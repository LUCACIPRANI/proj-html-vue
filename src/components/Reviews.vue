<template>
  <div class="column">
      <p class="info">{{ info.description }}</p>
      <img :src="require('../assets/' + info.src)" :alt="info.name" />
      <h3 class="info">{{ info.name }}</h3>
  </div>
</template>

<script>
export default {
  name: "Reviews",
  props: ["info"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "~@fortawesome/fontawesome-free/css/all.min.css";
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";

.column {
  height: 400px;
  width: 400px;
  margin-top: 70px;
  padding: 20px 60px;
  img{
    height: 120px;
    width: 120px;
    object-fit: cover;
    border-radius: 50%;
  }
  .info {
    align-self: flex-start;
    text-align: center;
  }
  h3{
    color: $btnColor;
    padding: 10px 0;
    line-height: 2.4rem;
  }
  p{
    color: $secondTitle;
    @include parag();
    padding: 10px 0;
    line-height: 2rem;
  }
}
</style>
