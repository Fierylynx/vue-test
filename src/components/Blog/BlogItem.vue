<template>
  <li class="blog__item" v-for="blog in blogs">
    <article class="blog__atricle">
      <div class="blog__image">
        <img :src="blog.image" alt="" />
      </div>
      <div class="blog__wrapper">
        <h4 class="blog__title subtitle">
          {{ blog.title }}
        </h4>
        <div class="blog__content">
          <p>
            {{ blog.content }}
          </p>
        </div>
        <button class="blog__button button">Read more</button>
      </div>
    </article>
  </li>
</template>

<script>
export default {
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

<style lang='scss'>

.blog__image {
  margin-bottom: 10px;
}

.blog__content {
  margin-bottom: 10px;
}

.blog__wrapper {
    @media (min-width: 767px) {
      max-width: 565px;
  }
}

</style>
