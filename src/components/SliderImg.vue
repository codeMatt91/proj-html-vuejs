<template>
  <div class="slider">
    <div class="container">
      <div
        class="partners d-flex justify-content-center py-4 border-top"
        
      >
        <i class="fa fa-angle-left position-relative" @click="next"></i>
        <div class="card-img" v-for="(slider, i) in filteredSliders" :key="i">
          <figure class="d-flex justify-content-center">
            <img 
              :src="require(`../assets/images/clients_partner_${slider}`)"
              alt="logo partner"
            />
          </figure>
        </div>
        <i class="fa fa-angle-right position-relative" @click="prev"></i>
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
      currentIndex: 0,
    };
  },
  methods: {
    next() {
      if (this.currentIndex === this.filteredSliders.length - 1)
        this.currentIndex = 0;
      this.currentIndex += 1;
    },
    prev() {
      if (this.currentIndex === 0)
        this.currentIndex = this.filteredSliders.length - 1;
      this.currentIndex -= 1;
    },
  },
  computed: {
    filteredSliders() {
      const sliders = this.sliders;
      return sliders.filter((el, i) => i <= 3);
    },
    // setImg(i) {
    //   return (this.currentIndex = i);
    // },
  },
};
</script>

<style lang="scss" scoped>
img {
  width: 50%;
}
</style>
