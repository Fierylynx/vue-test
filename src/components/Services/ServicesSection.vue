<template>
  <section class="services section-padding">
    <List />
  </section>
</template>

<script>
import List from "@/components/Services/ServiceList";
export default {
  components: {
    List,
  },
    data() {
    return {
      services: [
        {
          id: 1,
          title: "Photos",
          content:
            "Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac. Tempus leo erat, sit amet ullamcorper nisl.",
          image: require("@/assets/image/services/1.png"),
        },
        {
          id: 2,
          title: "Videos",
          content:
            "Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac. Tempus leo erat, sit amet ullamcorper nisl.",
          image: require("@/assets/image/services/2.png"),
        },
        {
          id: 3,
          title: "Downloads",
          content:
            "Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac. Tempus leo erat, sit amet ullamcorper nisl.",
          image: require("@/assets/image/services/3.png"),
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.services {
  &.section-padding {
    padding: 70px 0;
  }
}
</style>
