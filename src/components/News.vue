<template>
  <div class="news pb-5">
    <div class="container">
      <Heading :newstitle="news.title" />
      <div class="cards d-flex justify-content-between">
        <div
          class="card text-center border-0"
          v-for="(card, i) in news.cards"
          :key="i"
        >
          <img
            :src="require(`../assets/images/${card.src}`)"
            alt="image work"
          />
          <div class="title pt-3 fw-bold h5">{{ card.heading }}</div>
          <div id="subtitle">November 1st, 2017</div>
          <div class="text py-4">
            ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et
            scelerisque sem. Nunc molestie neque augue, at gravida mi blandit
          </div>
        </div>
      </div>
      <div class="d-flex justify-content-center pt-4">
        <a href="#" class="btn btn-orange">GO TO NEWS</a>
      </div>
    </div>
  </div>
</template>

<script>
import Heading from "./Heading";

export default {
  name: "News",
  props: ["news"],
  components: {
    Heading,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_vars.scss";
@import "../assets/scss/_utils.scss";
.news {
  background-color: $alabaster;
}

.card {
  width: 30%;
  background-color: $alabaster;
  .title {
    color: $yellow-orange;
  }
  #subtitle {
    font-size: 11px;
    color: grey;
  }
  .text {
    color: darkgray;
  }
}
a {
  font-size: 15px;
}
</style>
