<template>
    <div class="elements">
       <img :src="require('../assets/' + info.src)" :alt="info.title" />
        <div class="info">
          <h1>{{ info.title }}</h1>
          <h3>{{ info.description }}</h3>
        </div>
    </div>
</template>

<script>
export default {
  name: "Recent",
  props: ["info"],
};
</script>

<style scoped lang="scss">
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";

.elements {
  width: 35%;
  margin: 50px 15px;
  img{
    height: 250px;
    width: 100%;
    object-fit: cover;
  }
  .info {
  align-self: flex-start;
  text-align: center;
  line-height: 1.7rem;
  h1{
    color: $btnColor;
    padding: 10px 0;
    line-height: 2.4rem;
  }
  h3{
    color: $secondTitle;
  }
  img:last-child{
    padding-bottom: 70%;
  }
  }
}
</style>
