<template>
  <nav>
    <ul class="list-unstyled d-flex m-0">
      <li v-for="(navigation, index) in navigations" :key="index">
        <a
          class="text-decoration-none py-3 mx-2"
          :class="[navigation.hasClass ? 'text-white' : 'text-black']"
          href="navigation.link"
          >{{ navigation.text }}</a
        >
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Nav",
  data() {
    return {};
  },
  props: ["navigations"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
@import "../assets/scss/utils.scss";

li:last-child a {
  border-radius: 30px;
  background-color: $yellow-orange;
  padding: 15px;
  font-size: 14px;
}
</style>
