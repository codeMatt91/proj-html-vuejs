<template>
  <div class="text-center py-5 d-flex flex-column align-items-center">
    <h2 class="w-50 fw-bold">
      {{
        seotitle ||
        servicetitle ||
        worktitle ||
        planstitle ||
        newstitle ||
        "Start Your Free Consultation"
      }}
    </h2>
    <div class="text w-50">
      Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium
      doloremque laudantium.
    </div>
  </div>
</template>

<script>
export default {
  name: "Heading",
  props: ["seotitle", "servicetitle", "worktitle", "planstitle", "newstitle"],
};
</script>

<style scoped lang="scss">
h2 {
  padding: 30px 0;
}
</style>
