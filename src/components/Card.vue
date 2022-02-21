<template>
  <div>
    <i class="fa-2x pb-5" :class="card.icon"></i>
    <h4 class="fw-bold">{{ card.heading }}</h4>
    <div>{{ card.text }}</div>
    <div class="link" v-if="card.link">
      <a href="#"> Read More ></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["card"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
@import "../assets/scss/_utils.scss";
.fab,
.fas {
  color: $yellow-orange;
}
.link {
  padding: 12px 0;
  a {
    color: $yellow-orange;
    text-decoration: none;
  }
}
</style>
