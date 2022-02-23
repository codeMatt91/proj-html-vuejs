<template>
  <div class="modal">
    <div class="modal-content">
      <div class="modal-header">
        <Heading :pricetitle="price.title" :pricesub="price.subtitle" />
        <button type="button" class="btn-close"></button>
      </div>
      <!-- # Modal body: flexible about content -->
      <div class="modal-body">
        <slot></slot>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary">Close</button>
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
.modal {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}
</style>
