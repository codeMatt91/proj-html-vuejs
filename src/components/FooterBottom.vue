<template>
  <div class="footer-bottom py-5 text-dark">
    <div class="container text-center">
      <figure class="pb-4">
        <img src="../assets/images/logo_seo_1x.png" alt="logo avadaseo" />
      </figure>
      <div class="nav d-flex justify-content-center align-items-center">
        <Nav :navigations="navigations" />
        <a href="#" class="btn">Get in touch now</a>
      </div>
      <div class="copyright py-5 d-flex justify-content-center">
        &copy; Copyright 2012-2020 | Avadatheme by
        <strong>ThemeFusion</strong> | All Right Reserved | Powered by<strong
          >WordPress</strong
        >
      </div>
      <div>
        <i
          class="fs-4 mx-3"
          v-for="(icon, i) in icons"
          :key="i"
          :class="`fab fa-${icon}`"
        ></i>
      </div>
    </div>
  </div>
</template>

<script>
import Nav from "./Nav.vue";

export default {
  name: "FooterBottom",
  props: ["navigations"],
  components: {
    Nav,
  },
  data() {
    return {
      icons: ["facebook-f", "instagram", "twitter", "youtube"],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_vars.scss";
@import "../assets/scss/utils.scss";

.footer-bottom a {
  color: black;
}
.btn:hover {
  color: $yellow-orange;
}
.nav,
.copyright {
  font-size: 13px;
  color: $regent-gray;
}
i {
  color: $regent-gray;
}
</style>
