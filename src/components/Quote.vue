<template>
  <div class="quote section-padding section-bg">
    <div class="container">
      <blockquote class="quote__content">
        <p>
          In hac habitasse platea dictumst. Phasellus finibus ipsum enim, non
          pretium massa mattis non. Curabitur ut tempus ex. Nunc dictum est
          enim, consectetur convallis odio mollis tempus!
        </p>
        <cite class="quote__author top-element"> Jim Gordon (GCPD) </cite>
      </blockquote>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/vars";

.quote__content {
  position: relative;
  padding-top: 40px;
  font-style: italic;
  color: $white;
  background-image: url(../assets/image/quote-bg.png);
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;

  & p {
    margin-bottom: 20px;
  }

  &::before {
    position: absolute;
    top: 0;
    left: 0;
    content: "";
    width: 38px;
    height: 29px;
    background-image: url(../assets/image/svg/quote.svg);
    background-size: cover;
  }

  @media (min-width: 767px) {
    max-width: 766px;
    margin: 0 auto;
  }

  @media (min-width: 1169px) {
    padding-top: 50px;
    font-size: 28px;
    & p {
      margin-bottom: 55px;
    }
    &::before {
      width: 48px;
      height: 39px;
    }
  }
}

.quote__author {
  display: block;
  font-size: 16px;
  font-weight: 500;
  font-style: normal;
  color: $grey4;

  &.top-element {
    padding-top: 10px;
    &::before {
      background-color: $grey4;
    }
  }
  @media (min-width: 1169px) {
    font-size: 20px;
  }
}
</style>
