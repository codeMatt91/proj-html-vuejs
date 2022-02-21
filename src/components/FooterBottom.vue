<template>
  <div class="footer-bottom py-5 text-dark">
    <div class="container text-center">
      <figure class="pb-4">
        <img src="../assets/images/logo_seo_1x.png" alt="logo avadaseo" />
      </figure>
      <div class="d-flex justify-content-center align-items-center">
        <Nav :navigations="navigations" />
        <a href="#" class="btn">Get in touch now</a>
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
</style>
