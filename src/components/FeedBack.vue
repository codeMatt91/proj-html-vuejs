<template>
  <div class="feed-back">
    <div class="container">
      <h3 class="fw-bold text-center p-5">{{ feed.title }}</h3>
      <div v-for="(ticket, i) in feed.tickets" :key="i">
        <div
          v-if="i === currentIndex"
          class="ticket d-flex align-items-center flex-column text-center"
        >
          <img :src="require(`../assets/images/${ticket.img}`)" alt="" />
          <div class="text w-50 pt-4">{{ ticket.slogan }}</div>
          <div class="py-3">
            <span class="fw-bold">{{ ticket.name }}, </span>
            <span>{{ ticket.role }}</span>
          </div>
        </div>
      </div>
      <div class="slider-dots d-flex justify-content-center">
        <div
          class="dot"
          :class="[i === currentIndex ? 'active' : '']"
          v-for="(ticket, i) in feed.tickets"
          :key="i"
          @click="onClick(i)"
        ></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FeedBack",
  props: ["feed"],
  data() {
    return {
      active: "dot.active",
      currentIndex: 0,
    };
  },
  methods: {
    nextImage() {
      this.currentIndex++;
    },
    prevImage() {
      this.currentIndex--;
    },
    onClick(i) {
      this.currentIndex = i;
    },
  },
};
</script>

<style lang="scss" scoped>
.feed-back {
  padding-bottom: 80px;
}
.ticket {
  padding: 40px 0;
  img {
    width: 15%;
    border-radius: 50%;
  }
  .text {
    font-style: italic;
    color: grey;
  }
  animation: slide-in-fwd-center 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

@-webkit-keyframes slide-in-fwd-center {
  0% {
    -webkit-transform: translateZ(-1400px);
    transform: translateZ(-1400px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateZ(0);
    transform: translateZ(0);
    opacity: 1;
  }
}
@keyframes slide-in-fwd-center {
  0% {
    -webkit-transform: translateZ(-1400px);
    transform: translateZ(-1400px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateZ(0);
    transform: translateZ(0);
    opacity: 1;
  }
}

.slider-dots .dot {
  margin: 0 5px;
  height: 12px;
  width: 12px;
  border-radius: 50%;
  border: 1px solid black;
  cursor: pointer;
}

.slider-dots .dot.active {
  background-color: black;
}
</style>
