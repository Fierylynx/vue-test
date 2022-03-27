<template>
  <section class="hero section-bg">
    <div class="container">
      <div class="hero__wrapper">
        <h1 class="hero__title top-element">
          Title Of The Page
          <span class="hero__subtitle"> Subtitle </span>
        </h1>
        <div class="hero__content">
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam
            pharetra turpis tristique nisi laoreet gravida. Sed sed orci ut ante
            pellentesque efficitur id ac erat. Morbi metus metus, dictum sed
            arcu at, interdum porttitor erat.
          </p>
        </div>
        <button class="hero__button button" type="button">Button</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/vars";

.hero__wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100vh;

  @media (min-width: 767px) {
    max-width: 788px;
    margin: 0 auto;
  }
}

.hero__title {
  font-size: 32px;
  font-weight: 600;
  color: $white;
  text-transform: uppercase;

  @media (min-width: 767px) {
    font-size: 38px;
  }

  @media (min-width: 1169px) {
    font-size: 62px;
  }
}

.hero__subtitle {
  display: block;
  font-size: 22px;
  font-weight: 500;

  @media (min-width: 767px) {
    font-size: 28px;
  }

  @media (min-width: 1169px) {
    font-size: 30px;
  }
}

.hero__content {
  margin-bottom: 45px;
  color: $grey4;
  
  @media (min-width: 1169px) {
    font-size: 22px;
  }
}

.hero__button.button {
  @media (min-width: 1169px) {
    max-width: 200px;
    padding: 10px 0;
  }
}
</style>
