<template>
  <section class="services section-padding">
    <ul class="services__list">
      <article class="services__article" v-for="service in services">
        <li class="services__item">
          <h4 class="services__subtitle">{{ service.title }}</h4>
          <div class="services__content">
            <p>
              {{ service.content }}
            </p>
          </div>
          <button class="services__button button">Button</button>
        </li>
      </article>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      services: [
        {
          id: 1,
          title: "Photos",
          content:
            "Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac. Tempus leo erat, sit amet ullamcorper nisl.",
        },
        {
          id: 2,
          title: "Videos",
          content:
            "Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac. Tempus leo erat, sit amet ullamcorper nisl.",
        },
        {
          id: 3,
          title: "Downloads",
          content:
            "Vestibulum suscipit tortor magna, quis pellentesque arcu volutpat ac. Tempus leo erat, sit amet ullamcorper nisl.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.services__list {
  display: grid;
  gap: 60px;
}

.services__article {
  position: relative;
  max-width: 363px;
  width: 100%;
  margin: 0 auto;
  padding: 100px 53px 60px;
  background-color: #f6f6f6;
  border-radius: 6px;
  text-align: center;

  &::before {
    position: absolute;
    top: 0;
    content: '';
    width: 40px;
    height: 32px;
    background-image: url(../assets/services/1.png);
  }
}

.services__subtitle {
  margin-bottom: 20px;
  font-size: 22px;
  font-weight: 600;
  color: #353a3f;
  text-transform: uppercase;
}

.services__content {
  margin-bottom: 28px;
}
</style>
