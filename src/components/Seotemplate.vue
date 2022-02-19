<template>
  <div class="container h-100">
    <Heading :seotitle="seoTitle" :seosub="seoSub" class="my-5" />
    <div class="cards d-flex justify-content-around">
      <div
        class="card text-center border-0 px-5"
        v-for="(card, i) in cards"
        :key="i"
      >
        <i class="fas fa-road fa-2x pb-3"></i>
        <h3 class="fw-bold">{{ card.heading }}</h3>
        <div>{{ card.text }}</div>
      </div>
    </div>
  </div>
</template>

<script>
import Heading from "./Heading.vue";
export default {
  name: "Seotemplate",
  components: {
    Heading,
  },
  props: ["seo"],
  data() {
    return {
      seoTitle: "",
      seoSub: "",
      cards: [],
    };
  },
  methods: {
    getData() {
      const data = { ...this.seo };
      this.seoTitle = data.title;
      this.seoSub = data.subtitle;
      this.cards = data.cards;
    },
  },
  mounted() {
    this.getData();
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
@import "../assets/scss/_utils.scss";
.container {
  padding-bottom: 400px;
  background-image: url("../assets/images/agency-seo-desk-front-800x380.jpg");
  background-repeat: no-repeat;
  background-position: bottom;
}
.fas {
  color: $yellow-orange;
}
</style>
