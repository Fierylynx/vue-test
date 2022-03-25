<template>
  <section class="services section-padding">
    <div class="container">
      <ul class="services__list" :services="services">
        <Item
          v-for="(service, i) in services"
          :key="i"
          :title="service.title"
          :content="service.content"
          :image="service.image"
        />
      </ul>
    </div>
  </section>
</template>

<script>
import Item from "@/components/Services/ServiceItem";
export default {
  props: {
    services: {
      type: Array,
      required: true,
    },
  },
  components: {
    Item,
  },
  data() {
    return {
      services: [
        {
          id: 1,
          title: "Photos",
          content:
            "Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac. Tempus leo erat, sit amet ullamcorper nisl.",
          image: require("@/assets/image/svg/image.svg"),
        },
        {
          id: 2,
          title: "Videos",
          content:
            "Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac. Tempus leo erat, sit amet ullamcorper nisl.",
          image: require("@/assets/image/svg/video.svg"),
        },
        {
          id: 3,
          title: "Downloads",
          content:
            "Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac. Tempus leo erat, sit amet ullamcorper nisl.",
          image: require("@/assets/image/svg/download.svg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.services__list {
  display: grid;
  gap: 60px;
  justify-content: center;

  @media (min-width: 767px) {
    grid-template-columns: repeat(2, 363px);
    gap: 20px;
    row-gap: 60px;
  }

  @media (min-width: 1169px) {
    grid-template-columns: repeat(3, 1fr);
    justify-items: center;
  }
}
</style>
