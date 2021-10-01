<template>
  <main class="menu-container">
    <!-- section award  -->
    <div class="award">
      <div class="sm_title">AWARD WINNING</div>
      <div class="title">Pro Barbers</div>
      <div class="btn">MEET YOUR NEW BARBER</div>
    </div>
    <!-- section services  -->
    <div class="container_service">
      <div class="sm_title">MENS GROOMING</div>
      <div class="title">Services</div>
      <div class="products">
        <Services
          v-for="(service, index) in services"
          :key="'s' + index"
          :info="service"
        />
      </div>
      <div class="btn">READ ABOUT OUR SERVICES</div>
    </div>
    <!-- section grooming  -->
    <div class="container_grooming">
      <div class="sm_title">WE HAVE YOU COVERED</div>
      <div class="title">Avada Grooming Products</div>
      <div class="cont-grooming">
        <Grooming
          v-for="(groom, index) in grooming"
          :key="'g' + index"
          :info="groom"
        />
      </div>
      <div class="btn">SHOP OUR PRODUCT RANGE</div>
    </div>
    <!-- begin container shave- review -->
    <div class="main-container">
      <!-- section shaving  -->
      <div class="container-Shave">
        <div class="left">
          <img src="../assets/images/shaving_butter.png" alt="" />
        </div>
        <div class="right">
          <div class="sm_title">THIS MONTHS FEATURES PRODUCT</div>
          <div class="title">Shaving Butter</div>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores
            ducimus dolore iure, eos cupiditate officiis adipisci quam, nesciunt
            veritatis tempora porro cum esse.
          </p>
          <div class="btn">BUY NOW</div>
        </div>
      </div>
      <!-- section Reviews  -->
      <div class="container-review">
        <div class="reviews">
          <div class="sm_title">WHAT PEOPLE SAY</div>
          <div class="title">Reviews</div>
          <div class="rev">
            <Reviews
              v-for="(review, index) in reviews"
              :key="'re' + index"
              :info="review"
            />
          </div>
        </div>
      </div>
      <!-- end container shave- review -->
    </div>
    <!-- section recent  -->
    <div class="container_recent">
      <div class="sm_title">TALES FROM THE BARBER SHOP</div>
      <div class="title">Recent Blog posts</div>

      <div class="recent">
        <Recent
          v-for="(rec, index) in recent"
          :key="'rec' + index"
          :info="rec"
        />
      </div>
      <div class="btn">READ MORE FROM OUR BLOG</div>
    </div>
  </main>
</template>

<script>
// import js objects
import servicesD from "@/datas/services.js";
import grooming from "@/datas/grooming.js";
import reviews from "@/datas/reviews.js";
import recent from "@/datas/recent.js";

// import vue file
import Services from "./Services.vue";
import Grooming from "./Grooming.vue";
import Reviews from "./Reviews.vue";
import Recent from "./Recent.vue";

export default {
  name: "Main",
  data() {
    return {
      services: servicesD,
      grooming: grooming,
      reviews: reviews,
      recent: recent,
    };
  },
  props: {},
  components: {
    Services,
    Grooming,
    Reviews,
    Recent,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "~@fortawesome/fontawesome-free/css/all.min.css";
@import "@/styles/mixin.scss";
@import "@/styles/general.scss";
@import "@/styles/vars.scss";
.menu-container {
  height: 570vh;
  //   position: fixed;
  //   overflow-y: visible;
}
// section award
.award {
  height: 9%;
  background-image: url("../assets/images/intro-bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  @include centerC();
  .sm_title {
    @include sm-title();
  }
  .title {
    @include title();
  }
  .btn {
    @include btn();
    width: 20%;
    padding: 18px;
  }
}
// section services
.container_service {
  background-color: $firstTitle;
  height: 22%;
  @include startCol();
  .sm_title {
    @include sm-title();
  }
  .title {
    @include title();
  }
  p {
    @include parag();
  }
  .btn {
    @include btn();
    padding: 18px 20px;
    width: 22%;
    background-color: $firstTitle;
  }
  .products {
    @include centerR();
  }
}
// section Grooming
.container_grooming {
  height: 21%;
  background-image: url("../assets/images/avadabarbers-reviewsbackground.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  @include startCol();
  .cont-grooming {
    width: 85%;
    @include centerR();
    margin: 60px 0;
  }
  .sm_title {
    @include sm-title();
  }
  .title {
    @include title();
  }
  .btn {
    @include btn();
    width: 25%;
    padding: 18px;
  }
}
// section shave & section review
.main-container {
  height: 27%;
  position: relative;
  // section Shaving
  .container-Shave {
    position: absolute;
    top: -40px;
    left: 10%;
    height: 35%;
    background-image: url("../assets/images/avada.jpg");
    background-size: contain;
    background-repeat: no-repeat;
    background-color: $firstTitle;
    border-top: 4px solid $btnColor;
    width: 80%;
    margin: 0 auto;
    @include centerR();
    .left {
      height: 100%;
      width: 40%;
      @include centerR();
      img {
        object-fit: contain;
        height: 400px;
        width: 400px;
      }
    }
    .right {
      width: 60%;
      height: 100%;
      padding: 5rem;
      background-color: $footerDown;
      .sm_title {
        @include sm-title();
      }
      .title {
        @include title();
        padding-bottom: 15px;
      }
      p {
        @include parag();
      }
      .btn {
        @include btn();
        width: 30%;
        padding: 15px 30px;
        background-color: $footerDown;
      }
    }
  }
  // section reviews
  .container-review {
    height: 90%;
    position: relative;
    .rev {
      @include centerR();
    }
    .reviews {
      @include startCol();
      position: absolute;
      top: 650px;
      left: 50%;
      transform: translate(-50%, -50%);
    }
    .sm_title {
      text-align: center;
      @include sm-title();
    }
    .title {
      @include title();
    }
  }
}
// section recent
.container_recent {
  height: 21%;
  background-color: #f5f5f5;
  @include startCol();
  .recent {
    @include centerR();
    width: 80%;
  }
  .sm_title {
    @include sm-title();
  }
  .title {
    @include title();
  }
  .btn {
    @include btn();
    padding: 18px 20px;
    background-color: #f5f5f5;
  }
}
</style>
