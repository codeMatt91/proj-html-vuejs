<template>
  <div class="footer-top text-white">
    <div id="filter" class="">
      <div class="container">
        <Heading />
        <div class="button d-flex justify-content-center">
          <a href="#" class="btn btn-orange"> CONTACT US NOW</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Heading from "./Heading.vue";
export default {
  name: "FooterTop",
  components: {
    Heading,
  },
};
</script>

<style lang="scss" scoped>
.footer-top {
  background-image: url("../assets/images/CTA-seo-1.jpg");
  background-position: center;
  background-size: cover;
}
#filter {
  background-color: rgba(0, 0, 0, 0.5);
}

.button {
  padding-bottom: 70px;
}
</style>
