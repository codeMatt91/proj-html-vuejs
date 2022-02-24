<template>
  <div class="modale">
    <div class="content">
      <div class="modale-header text-white">
        <Heading :pricetitle="price.title" :pricesub="price.subtitle" />
        <button type="button" class="btn-close"></button>
      </div>
      <!-- # Modal body: flexible about content -->
      <div class="modale-body">
        <slot></slot>
      </div>
      <div class="modale-footer">
        <button type="button" class="btn btn-secondary" @click="$emit('clicked')">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</template>

<script>
import Heading from "./Heading.vue";

export default {
  name: "Modal",
  components: {
    Heading,
  },
  props: ["price"],
};
</script>

<style lang="scss" scoped>
.modale {
  z-index: 5;
  background-color: rgba($color: #000000, $alpha: 0.8);
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
