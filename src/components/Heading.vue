<template>
  <div class="text-center py-5 d-flex flex-column align-items-center">
    <h2 class="w-50 fw-bold">
      {{ seotitle || servicetitle || worktitle || planstitle }}
    </h2>
    <div class="text w-50">
      {{ seosub || servicesub || worksub || planssub }}
    </div>
  </div>
</template>

<script>
export default {
  name: "Heading",
  props: [
    "seotitle",
    "seosub",
    "servicetitle",
    "servicesub",
    "worktitle",
    "worksub",
    "planstitle",
    "planssub",
  ],
};
</script>

<style scoped lang="scss">
h2 {
  padding: 30px 0;
}
</style>
