<template>
  <div class="plans pb-5">
    <div class="container">
      <Heading
        :planstitle="plans.title"
        :planssub="plans.subtitle"
        class="text-white"
      />
      <div class="cards d-flex justify-content-between">
        <div
          class="card p-4 text-center bg-white"
          v-for="(card, i) in plans.cards"
          :key="i"
        >
          <h4 class="fw-bold py-3">{{ card.title }}</h4>
          <div
            id="price"
            class="position-relative d-flex justify-content-center py-3"
          >
            <div class="position-relative">
              <div class="dollar position-absolute">$</div>
            </div>
            <div id="month-value">
              {{ card.price }}
            </div>
            <div class="monthly position-relative">
              <div class="month position-absolute">/monthly</div>
              <div id="cent">99</div>
            </div>
          </div>
          <div class="p-2">{{ card.project }} Project</div>
          <div class="p-2">{{ card.storage }} GB Storage</div>
          <div class="p-2">Unlimited Users</div>
          <div class="text-center">
            <a href="#" class="btn btn-white fw-bold m-3">START TODAY</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Heading from "./Heading.vue";

export default {
  name: "Plans",
  props: ["plans"],
  components: {
    Heading,
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
@import "../assets/scss/_utils.scss";

.plans {
  background-image: url("../assets/images/background1.jpg");
  background-size: cover;
}
.card {
  width: 23%;
  a {
    color: $regent-gray;
    font-size: 15px;
    color: $scorpion;
    border: 2px groove $regent-gray;
    &:hover {
      background-color: $yellow-orange;
      color: white;
      border: 0 groove $yellow-orange;
    }
  }
  #month-value {
    color: $science-blu;
    font-size: 35px;
    font-weight: bold;
  }
  #cent {
    color: $science-blu;
    font-size: 12px;
    position: absolute;
    left: 0;
    top: 5px;
  }
}
.monthly {
  font-size: 8px;
  height: 100%;
  position: relative;
  .month {
    bottom: 10px;
  }
}
.dollar {
  left: -10px;
}
</style>
