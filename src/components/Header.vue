<template>
  <header class="py-4">
    <div class="container">
      <div
        class="header-top d-flex align-items-center justify-content-between pt-3"
      >
        <img src="../assets/images/logo_seo_w_1x.png" alt="logo AvadaSeo" />
        <div class="d-flex align-items-center">
          <Nav :navigations="navigations" :apply="apply" />
          <a href="#" class="btn btn-orange">GET IN TOUCH NOW</a>
        </div>
      </div>
      <div class="header-bottom">
        <div class="row">
          <div class="col-6 d-flex align-items-center">
            <div>
              <h1>
                SEM Campaigns Made <br />
                Simple With Avada
              </h1>
              <div class="pb-4">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae
                expedita cumque accusantium laboriosam eos error? Voluptatibus
                adipisci illo est veritatis numquam excepturi.
              </div>
              <a class="btn btn-orange">BUY AVADA NOW</a>
              <a class="btn btn-blu">CONTACT US</a>
            </div>
          </div>
          <div class="col-6"></div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import Nav from "./Nav.vue";
export default {
  name: "Header",
  data() {
    return {
      apply: true,
    };
  },
  components: {
    Nav,
  },
  props: ["navigations"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
@import "../assets/scss/utils.scss";

header {
  background-image: url("../assets/images/1-hero-image.png");
  background-position: center;
  background-size: cover;
  background-repeat: repeat-y;
  color: $t-white;
}
.header-top .btn {
  font-size: 15px;
}
.header-top {
  animation: puff-in-center 1.2s cubic-bezier(0.47, 0, 0.745, 0.715);
}

@-webkit-keyframes puff-in-center {
  0% {
    transform: scale(2);
    transform: scale(2);
    filter: blur(4px);
    filter: blur(4px);
    opacity: 0;
  }
  100% {
    transform: scale(1);
    transform: scale(1);
    filter: blur(0px);
    filter: blur(0px);
    opacity: 1;
  }
}
@keyframes puff-in-center {
  0% {
    transform: scale(2);
    transform: scale(2);
    filter: blur(4px);
    filter: blur(4px);
    opacity: 0;
  }
  100% {
    transform: scale(1);
    transform: scale(1);
    filter: blur(0px);
    filter: blur(0px);
    opacity: 1;
  }
}

.header-bottom {
  padding: 300px 0;
  animation: puff-in-center 1.2s cubic-bezier(0.47, 0, 0.745, 0.715);
}
@-webkit-keyframes puff-in-center {
  0% {
    transform: scale(2);
    transform: scale(2);
    filter: blur(4px);
    filter: blur(4px);
    opacity: 0;
  }
  100% {
    transform: scale(1);
    transform: scale(1);
    filter: blur(0px);
    filter: blur(0px);
    opacity: 1;
  }
}
@keyframes puff-in-center {
  0% {
    transform: scale(2);
    transform: scale(2);
    filter: blur(4px);
    filter: blur(4px);
    opacity: 0;
  }
  100% {
    transform: scale(1);
    transform: scale(1);
    filter: blur(0px);
    filter: blur(0px);
    opacity: 1;
  }
}
</style>
