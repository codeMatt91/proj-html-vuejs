<template>
  <div class="news">
    <div class="containe">
      <Heading :newstitle="news.title" />
      
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
  background-color: $concrete;
}
</style>
