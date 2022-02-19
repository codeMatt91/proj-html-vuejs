<template>
  <main>
    <Seotemplate :seo="dataSeo" />
    <Service :service="dataService" />
  </main>
</template>

<script>
import Seotemplate from "./Seotemplate";
import Service from "./Service.vue";
export default {
  name: "Main",
  components: {
    Seotemplate,
    Service,
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
          },
          {
            icon: "fa-video",
            heading: "Brand Strategy",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et dapibus faucibus odio.",
          },
          {
            icon: "fa-tint",
            heading: "Local SEO",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et dapibus faucibus odio.",
          },
          {
            icon: "fa-tint",
            heading: "SEO Analysis",
            text: "Vestibulum in lacinia metus. Suspendisse in enim ipsum. Nulla facilisi. Donec ante turpis, dictum sed magna et dapibus faucibus odio.",
          },
        ],
      },
    };
  },
};
</script>

<style scoped lang="scss"></style>
