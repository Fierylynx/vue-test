<template>
  <ul class="services__list">
    <Item v-for="service in services"/>
  </ul>
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
};
</script>

<style lang="scss">
.services__list {
  display: grid;
  gap: 60px;
  justify-content: center;
    @media (min-width: 767px) {
      grid-template-columns: 363px 363px;
      gap: 20px;
      row-gap: 60px;
  }
}
</style>
