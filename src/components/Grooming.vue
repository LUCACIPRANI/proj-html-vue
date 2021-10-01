<template>
  <div class="grooming">
    <img :src="require('../assets/' + info.src)" :alt="info.title" />
    <div class="info">
      <h1>{{ info.title }}</h1>
      <h3>{{ info.price }}</h3>
    </div>
  </div>
</template>

<script>
// import
export default {
  name: "Grooming",
  props: ["info"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";

.grooming {
  @include centerC();
}
img {
  height: 300px;
  width: 300px;
  object-fit: contain;
}
.info {
  align-self: flex-start;
  text-align: start;
  color: $btnColor;
  line-height: 2.2rem;
}
</style>
