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
        { link: "#", text: "Home", hasClass: true },
        { link: "#", text: "Who We Do", hasClass: true },
        { link: "#", text: "What We Do", hasClass: true },
        { link: "#", text: "Where We Work", hasClass: true },
        { link: "#", text: "Careers", hasClass: true },
        { link: "#", text: "News", hasClass: true },
        { link: "#", text: "GET IN TOUCH NOW", hasClass: true },
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
