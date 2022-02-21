<template>
  <main>
    <Seotemplate :seo="dataSeo" />
    <Service :service="dataService" />
    <Work :work="dataWork" />
    <Plans :plans="dataPlans" />
    <News :news="dataNews" />
    <FeedBack :feed="dataFeed" />
    <SliderImg :sliders="dataSlider"/>
  </main>
</template>

<script>
import Seotemplate from "./Seotemplate";
import Service from "./Service.vue";
import Work from "./Work.vue";
import Plans from "./Plans.vue";
import News from "./News.vue";
import FeedBack from "./FeedBack.vue";
import SliderImg from "./SliderImg.vue";

export default {
  name: "Main",
  components: {
    Seotemplate,
    Service,
    Work,
    Plans,
    News,
    FeedBack,
    SliderImg,
  },
  data() {
    return {
      dataSeo: {
        title: "Meet The New Agency SEO Template From The Avada Team",
        cards: [
          {
            icon: "fa-road",
            heading: "Establish Goals",
            text: "Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis mi ligula euismod odio vel dictum mi risus a mi.",
          },
          {
            icon: "fa-video",
            heading: "Work With a Team",
            text: "Cras semper auctor aliquam. Sed porta sed lacus sit amet consectetur. Lorem ipsum dolor sit amet consectetur adipisce.",
          },
          {
            icon: "fa-tint",
            heading: "Get Results",
            text: "Vestibulum scelerisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus.",
          },
        ],
      },
      dataService: {
        title: "See Our Top Notch Services",
        cards: [
          {
            icon: "fa-road",
            heading: "Google SEO",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et dapibus faucibus odio.",
            link: true,
          },
          {
            icon: "fa-video",
            heading: "Brand Strategy",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et dapibus faucibus odio.",
            link: true,
          },
          {
            icon: "fa-tint",
            heading: "Local SEO",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et dapibus faucibus odio.",
            link: true,
          },
          {
            icon: "fa-tint",
            heading: "SEO Analysis",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et dapibus faucibus odio.",
            link: true,
          },
        ],
      },
      dataWork: {
        title: "Our Work",
        images: [
          {
            link: "case-study-gallery-3-1-400x300.jpg",
          },
          {
            link: "case-study-gallery-2-400x300.jpg",
          },
          {
            link: "case-study-gallery-1-1-400x300.jpg",
          },
          {
            link: "case-study-gallery-4-1-400x300.jpg",
          },
          {
            link: "case-study-gallery-5-1-400x300.jpg",
          },
          {
            link: "case-study-gallery-6-1-400x300.jpg",
          },
        ],
      },
      dataPlans: {
        title: "Our Plans",
        cards: [
          { title: "Standard", price: 19, project: 5, storage: 5 },
          { title: "Premium", price: 29, project: 10, storage: 15 },
          { title: "Professional", price: 39, project: 15, storage: 30 },
          {
            title: "Extreme",
            price: 59,
            project: "Unlimited",
            storage: "Unlimited",
          },
        ],
      },
      dataNews: {
        title: "Our News",
        cards: [
          {
            src: "related-service-2-320x202.jpg",
            heading: "Why You Need A SEO Agency Now",
          },
          {
            src: "related-service-4-320x202.jpg",
            heading: "SEO Tips For Your Startup",
          },
          {
            src: "blog-post-6-320x202.jpg",
            heading: "Image Optimization For Your Site",
          },
        ],
      },
      dataFeed: {
        title: "What Our Clients Say",
        tickets: [
          {
            img: "testimonials-2.jpg",
            slogan:
              "Ability proceeds from a fusion of skills, knowledge, understanding and imagination, consolidated by experience.",
            name: "Luis Desalvo",
            role: "CREO TECH",
          },
          {
            img: "testimonials-1.jpg",
            slogan:
              "Beauty is when you can appreciate yourself. When you love yourself, that’s when you’re most beautiful.",
            name: "Shelia McCourtney",
            role: "ARCHITECT",
          },
        ],
      },
      dataSlider: [
        "1-200x202.png",
        "2-200x202.png",
        "3-200x202.png",
        "4-200x202.png",
        "5-200x202.png",
        "6-200x202.png",
      ],
    };
  },
};
</script>

<style scoped lang="scss"></style>
