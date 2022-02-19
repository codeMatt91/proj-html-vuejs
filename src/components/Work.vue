<template>
  <div class="work pb-5">
    <div class="container">
      <Heading :worktitle="work.title" :worksub="work.subtitle" />
      <div class="row gy-5">
        <div class="col-4" v-for="(image, i) in work.images" :key="i">
          <img :src="require(`../assets/images/${image.link}`)" alt="" />
        </div>
        <div class="d-flex justify-content-center">
          <a href="#" class="btn btn-orange">VIEW OUR WORK</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Heading from "./Heading.vue";
export default {
  name: "Work",
  components: {
    Heading,
  },
  props: ["work"],
};
</script>

<style scoped>
a{
   font-size: 15px;
}
</style>
