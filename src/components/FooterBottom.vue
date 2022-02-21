<template>
  <div class="footer-bottom py-5 text-dark">
    <div class="container d-flex justify-content-center">
      <img src="../assets/images/logo_seo_1x.png" alt="logo avadaseo" />
      <Nav :navigations="navigations" />
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

<style lang="scss" scoped></style>
