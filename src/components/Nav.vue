<template>
  <nav>
    <ul class="list-unstyled d-flex m-0">
      <li class="mx-2" v-for="(navigation, index) in navigations" :key="index">
        <a
          class="label text-decoration-none py-3 mx-2"
          :href="navigation.link"
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

nav a {
  color: inherit;
}
a:hover {
  color: $yellow-orange;
}
li:nth-child(5) a {
  padding-right: 50px;
}
</style>
