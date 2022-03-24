<template>
  <ul class="social">
    <Item />
  </ul>
</template>

<script>
import Item from '@/components/Social/SocialItem'
export default {
  components: {
    Item,
  }
};
</script>

<style lang="scss">
.social {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;

  li:not(:last-child) {
    margin-right: 30px;
  }
}
</style>
