<template>
  <footer>
    <FooterTop />
    <FooterBottom :navigations="navigations" />
  </footer>
</template>

<script>
import FooterTop from "./FooterTop.vue";
import FooterBottom from "./FooterBottom.vue";

export default {
  name: "Footer",
  props: ["navigations"],
  components: {
    FooterTop,
    FooterBottom,
  },
};
</script>

<style scoped lang="scss"></style>
