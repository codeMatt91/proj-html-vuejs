<template>
  <div id="seo">
    <div class="container">
      <Heading :seotitle="seoTitle" :seosub="seoSub" />
      <div class="cards d-flex justify-content-between">
        <div
          class="card text-center border-0 p-5"
          v-for="(card, i) in cards"
          :key="i"
        >
          <Card :card="card" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Heading from "./Heading.vue";
import Card from "./Card.vue";
export default {
  name: "Seotemplate",
  components: {
    Heading,
    Card,
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
#seo {
  background-color: $alabaster;
}
.fas {
  color: $yellow-orange;
}
</style>
