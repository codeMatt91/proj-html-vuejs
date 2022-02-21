<template>
  <div class="slider">
    <div class="container">
      <div class="partners py-4 border-top d-flex">
        <div class="card-img" v-for="(slider, i) in sliders" :key="i">
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
};
</script>

<style lang="scss" scoped>
img {
  width: 50%;
}
</style>
