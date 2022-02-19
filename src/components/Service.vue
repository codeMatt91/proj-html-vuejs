<template>
  <div class="service text-white">
    <div class="container">
      <Heading
        :servicetitle="this.service.title"
        :servicesub="this.service.subtitle"
      />
      <div class="cards d-flex justify-content-around">
        <div
          class="card text-center border-0 mx-3"
          v-for="(card, i) in service.cards"
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
  name: "Service",
  components: {
    Heading,
    Card,
  },
  props: ["service"],
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
@import "../assets/scss/_utils.scss";
.service {
  background-image: url("../assets/images/pattern_background.png");
  background-size: contain;
  background-color: $deep-cove;
  padding-bottom: 150px;
}
.card {
  background-color: $lucky-point;
  padding: 30px;
}
</style>
