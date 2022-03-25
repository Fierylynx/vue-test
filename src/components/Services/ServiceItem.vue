<template>
  <li class="services__item">
    <article class="services__article">
      <div class="services__image">
        <img :src="image" alt="image" />
      </div>
      <h4 class="services__subtitle subtitle">{{ title }}</h4>
      <div class="services__content">
        <p>
          {{ content }}
        </p>
      </div>
      <button class="services__button button" type="button">Button</button>
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
@import "../../assets/scss/vars";

.services__item {
  position: relative;
  max-width: 363px;
  width: 100%;
  margin: 0 10px;
  padding: 100px 53px 60px;
  background-color: #f6f6f6;
  border-radius: 6px;
  text-align: center;

  @media (min-width: 767px) {
    margin: 0;
  }
}

.services__article {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.services__image {
  position: absolute;
  top: -40px;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 80px;
  height: 80px;
  background-color: $white;
  border-radius: 40px;

  @media (min-width: 767px) {
    top: -55px;
    width: 110px;
    height: 110px;
    border-radius: 55px;
  }
}

.services__subtitle {
  margin-bottom: 20px;
}

.services__content {
  margin-bottom: 28px;
}
</style>
