<template>
  <ul class="social">
    <Item
      v-for="(social, i) in socials"
      :key="i"
      :image="social.image" 
    />
  </ul>
</template>

<script>
import Item from "@/components/Social/SocialItem";
export default {
  components: {
    Item,
  },
  props: {
    socials: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
@import "../../assets/scss/vars";
.social {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
}
</style>
