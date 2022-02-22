<template>
  <div>
    <Header :navigations="navs" />
    <Main />
    <Footer :navigations="navs" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      navs: [
        { link: "#", text: "Home" },
        { link: "#seo", text: "Who We Do" },
        { link: "#service", text: "What We Do" },
        { link: "#work", text: "Where We Work" },
        { link: "#plans", text: "Careers" },
        { link: "#news", text: "News" },
      ],
      headingFooter: {
        title: "Start Your Free Consultation",
        subTitle:
          "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
      },
    };
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
