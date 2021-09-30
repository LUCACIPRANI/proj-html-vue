<template>
  <footer>
    <div class="footer-top">
      <div class="column">
        <img src="../assets/images/left-ft.png" alt="" />
        <button class="btn">SHOP OUR RANGE NOW</button>
      </div>
      <div class="column">
        <img class="ct-img" src="../assets/images/logo.png" alt="" />
        <div class="contacts">
          Avada Barbers <br />
          123 New York Street <br />
          New York City <br />
          infoyourwebsite.com <br />
          +1 <span>555</span> 555-1212
        </div>
        <div class="followUs">FOLLOW US</div>
        <div class="social">
          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-twitter"></i>
          <i class="fab fa-youtube"></i>
          <i class="fab fa-instagram"></i>
        </div>
      </div>
      <div class="column">
        <img src="../assets/images/right-ft.png" alt="" />
        <button class="btn">BOOK YOUR APPOINTMENT</button>
      </div>
    </div>

    <div class="footer-down">
      <h5>
        © Copyright 2012-2020 | Avada Theme by ThemeFusion | All Rights Reserved
        | Powered by WordPress
      </h5>
      <i class="fas fa-chevron-up"></i>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";

footer {
  height: 85vh;
  .footer-top {
    @include centerR();
    height: 85%;
    background-color: $footerTop;
    .column {
      @include centerC();
      padding: 15px;
      margin: 0 30px;
      .social,
      .followUs {
        margin: 35px 0;
      }
      .ct-img {
        height: 200px;
        width: 200px;
        object-fit: contain;
        @include centerC();
      }
      img {
        height: 400px;
        width: 400px;
        object-fit: contain;
      }
      .contacts {
        color: $footerText;
        text-align: center;
        font-weight: 600;
        line-height: 1.4rem;
      }
      span::before {
        content: "(";
      }
      span::after {
        content: ")";
      }
      .followUs {
        color: $btnColor;
        font-weight: 800;
      }
      .btn {
        border: 2px solid $btnColor;
        color: $btnColor;
        background-color: $footerTop;
        padding: 12px 17px;
      }
      .social{
          color: white;
          .fab{
              padding: 8px;
          }
      }
    }
  }
  .footer-down {
    position: relative;
    @include centerC();
    height: 15%;
    background-color: $footerDown;
    text-align: center;
    color: $footerText;
    .fa-chevron-up{
        position: absolute;
        color: white;
        bottom: 0;
        right: 3%;
        background-color: #303030;
        padding: 7px 19px;
    }
  }
}
</style>
