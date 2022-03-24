<template>
  <ul class="blog__list">
    <Item />
  </ul>
</template>

<script>
import Item from "@/components/Blog/BlogItem";
export default {
  components: {
    Item,
  },
};
</script>

<style lang='scss'>

.blog__list {
  display: grid;
  gap: 60px;
}

</style>
