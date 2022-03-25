<template>
  <li class="blog__item">
    <article class="blog__atricle">
      <div class="blog__image">
        <img :src="image" alt="" />
      </div>
      <div class="blog__content">
        <h4 class="blog__subtitle subtitle">
          {{ title }}
        </h4>
        <div class="blog__text">
          <p>
            {{ content }}
          </p>
        </div>
        <button class="blog__button button">Read more</button>
      </div>
    </article>
  </li>
</template>

<script>
export default {
  props: {
    image: "",
    title: "",
    content: "",
  },
};
</script>

<style lang="scss">
.blog__atricle {
  @media (min-width: 1169px) {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}

.blog__image {
  width: 100%;
  margin: 0 0 10px 0;
  @media (min-width: 1169px) {
    margin: 0 20px 0 0;
  }
}

.blog__text {
  margin-bottom: 10px;
  @media (min-width: 1169px) {
    margin-bottom: 20px;
  }
}

.blog__content {
  @media (min-width: 767px) {
    max-width: 565px;
  }
}
</style>
