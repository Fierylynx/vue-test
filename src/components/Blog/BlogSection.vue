<template>
  <section class="blog section-padding">
    <div class="container">
      <div class="blog__wrapper">
        <h2 class="blog__title title top-element">From the blog</h2>
        <ul 
          class="blog__list"
          :blogs="blogs"
        >
          <BlogItem 
            v-for="(blog, i) in blogs"
            :key="i"
            :image="blog.image"
            :title="blog.title"
            :content="blog.content"
          />
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
import BlogItem from "@/components/Blog/BlogItem";
export default {
  components: {
    BlogItem,
  },
  props: {
    blogs: {
      type: Array,
      required: true,
    }
  },
  data() {
    return {
      blogs: [
        {
          id: 1,
          title: "Title of a post 1",
          content:
            "In hac habitasse platea dictumst. Phasellus finibus ipsum enim, non pretium massa mattis non. Curabitur ut tempus ex. Nunc dictum est enim, consectetur convallis odio mollis tempus.",
          image: require("@/assets/image/blog/image.jpg"),
        },
        {
          id: 2,
          title: "Title of a post 2",
          content:
            "In hac habitasse platea dictumst. Phasellus finibus ipsum enim, non pretium massa mattis non. Curabitur ut tempus ex. Nunc dictum est enim, consectetur convallis odio mollis tempus.",
          image: require("@/assets/image/blog/image.jpg"),
        },
        {
          id: 3,
          title: "Title of a post 3",
          content:
            "In hac habitasse platea dictumst. Phasellus finibus ipsum enim, non pretium massa mattis non. Curabitur ut tempus ex. Nunc dictum est enim, consectetur convallis odio mollis tempus.",
          image: require("@/assets/image/blog/image.jpg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.blog__title {
  margin-bottom: 30px;
  
  @media (min-width: 1169px) {
    margin-bottom: 70px;
  }
}

.blog__list {
  display: grid;
  gap: 60px;
  justify-content: center;

  @media (min-width: 1169px) {
    justify-content: normal;
  }
}
</style>
