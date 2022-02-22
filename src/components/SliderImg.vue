<template>
  <div class="slider">
    <div class="container">
      <div class="partners d-flex justify-content-center py-4 border-top">
        <div class="card-img" v-for="(slider, i) in filteredSliders" :key="i">
          <figure class="d-flex justify-content-center">
            <img
              :src="require(`../assets/images/clients_partner_${slider}`)"
              alt="logo partner"
            />
          </figure>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SliderImg",
  props: ["sliders"],
  data() {
    return {
      nextIndex: 3,
      prevIndex: 0,
    };
  },
  methods: {
    myFunction() {
      if (
        (this.prevIndex >= 0) & (this.prevIndex <= 3) &&
        (this.nextIndex >= 3) & (this.nextIndex <= 4)
      ) {
        this.prevIndex++;
        this.nextIndex++;
      } else {
        this.prevIndex--;
        this.nextIndex--;
      }
    },
  },
  computed: {
    filteredSliders() {
      const sliders = this.sliders;
      return sliders.filter(
        (el, i) => (i >= this.prevIndex) & (i <= this.nextIndex)
      );
    },
  },
  created() {
    setInterval(this.myFunction, 2000);
  },
};
</script>

<style lang="scss" scoped>
img {
  width: 40%;
}
</style>
