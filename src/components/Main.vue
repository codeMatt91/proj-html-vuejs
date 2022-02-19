<template>
  <main>
    <Seotemplate :seo="dataSeo" />
    <Service :service="dataService" />
    <Work :work="dataWork" />
  </main>
</template>

<script>
import Seotemplate from "./Seotemplate";
import Service from "./Service.vue";
import Work from "./Work.vue";
export default {
  name: "Main",
  components: {
    Seotemplate,
    Service,
    Work,
  },
  data() {
    return {
      dataSeo: {
        title: "Meet The New Agency SEO Template From The Avada Team",
        subtitle:
          "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
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
        subtitle:
          "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
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
        subtitle:
          "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
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
    };
  },
};
</script>

<style scoped lang="scss"></style>
