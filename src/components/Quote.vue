<template>
  <div class="quote section-padding">
    <blockquote class="quote__content">
      In hac habitasse platea dictumst. Phasellus finibus ipsum enim, non
      pretium massa mattis non. Curabitur ut tempus ex. Nunc dictum est enim,
      consectetur convallis odio mollis tempus!
      <cite class="quote__author top-element"> Jim Gordon (GCPD) </cite>
    </blockquote>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.quote {
  padding: 50px 0;
  background-color: #353a3f;
}

.quote__content {
  position: relative;
  padding-top: 40px;
  font-style: italic;
  color: #fff;

  &::before {
    position: absolute;
    top: 0;
    left: 0;
    content: '';
    width: 38px;
    height: 29px;
    background-image: url(../assets/svg/quote.svg);
    background-size: cover;
  }
}

.quote__author {
  display: block;
  font-size: 16px;
  font-weight: 500;
  font-style: normal;
  color: #8c9198;

  &.top-element {
    padding-top: 10px;
    &::before {
      background-color: #8c9198;
    }
  }
}
</style>
