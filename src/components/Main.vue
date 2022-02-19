<template>
  <main>
    <Seotemplate :seo="dataSeo" />
  </main>
</template>

<script>
import Seotemplate from "./Seotemplate";
export default {
  name: "Main",
  components: {
    Seotemplate,
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
    };
  },
};
</script>

<style scoped lang="scss"></style>
