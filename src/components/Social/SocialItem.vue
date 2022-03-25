<template>
  <li class="social__item">
    <a href="#">
      <img :src="image" alt="social svg" />
    </a>
  </li>
</template>

<script>
export default {
  props: {
    image: '',
  },
};
</script>

<style lang="scss">
.social__item {
  
  &:not(:last-child) {
    margin-right: 30px;
  }

  @media (min-width: 991px) {
    padding: 2px;
    transition: opacity 0.3s;

    &:hover {
      opacity: 0.8;
    }
  }
}
</style>
