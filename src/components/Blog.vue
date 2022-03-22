<template>
  <section class="blog section-padding">
    <ul class="blog__list">
      <article class="blog__atricle">
        <li class="blog__item" v-for="blog in blogs">
          <h4 class="blog__title">
            {{ blog.title }}
          </h4>
          <div class="blog__content">
            <p>
              {{ blog.content }}
            </p>
          </div>
        <button class="blog__button button">Read more</button>
        </li>
      </article>
    </ul>
  </section>
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
        },
        {
          id: 2,
          title: "Title of a post 2",
          content:
            "In hac habitasse platea dictumst. Phasellus finibus ipsum enim, non pretium massa mattis non. Curabitur ut tempus ex. Nunc dictum est enim, consectetur convallis odio mollis tempus.",
        },
        {
          id: 3,
          title: "Title of a post 3",
          content:
            "In hac habitasse platea dictumst. Phasellus finibus ipsum enim, non pretium massa mattis non. Curabitur ut tempus ex. Nunc dictum est enim, consectetur convallis odio mollis tempus.",
        },
      ],
    };
  },
};
</script>

<style></style>
