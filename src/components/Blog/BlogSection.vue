<template>
  <section class="blog section-padding">
    <div class="container">
      <h2 class="blog__title title top-element">From the blog</h2>
      <List />
    </div>
  </section>
</template>

<script>
import List from "@/components/Blog/BlogList";
export default {
  components: {
    List,
  },
};
</script>

<style></style>
