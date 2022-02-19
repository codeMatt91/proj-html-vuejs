<template>
  <div>
    <i class="fas fa-road fa-2x pb-3"></i>
    <h4 class="fw-bold">{{ card.heading }}</h4>
    <div>{{ card.text }}</div>
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

.fas {
  color: $yellow-orange;
}
</style>
