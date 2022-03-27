<template>
  <form class="menu__form">
    <input class="menu__input" type="text" v-show="inputVisibility" />
    <button
      class="menu__search menu__search--active"
      @click.prevent="inputVisibility = !inputVisibility"
      type="button"
      :class="{ active: inputVisibility }"
    ></button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      inputVisibility: false,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/scss/vars";

.menu__form {
  display: flex;
  align-items: center;
  justify-content: center;
    @media (min-width: 991px) {
    padding: 0 5px;
  }
}

.menu__input {
  width: 100%;
  padding: 6px;
  line-height: 1.8;
  border: none;
  border-radius: 4px 0 0 4px;
  outline: transparent;
  @media (min-width: 767px) {
    max-width: 700px;
  }
    @media (min-width: 991px) {
    max-width: 70px;
  }
}

.menu__search {
  position: relative;
  z-index: 100;
  width: 44px;
  height: 45px;
  padding: 2px;
  background-color: $grey3;
  border: none;
  border-radius: 4px;

  &.active {
    background-color: $grey3;
    border-radius: 0 4px 4px 0;
  }

  &::after {
    position: absolute;
    top: 7px;
    left: 6px;
    content: "";
    width: 30px;
    height: 30px;
    background-image: url(../../assets/image/svg/loupe.svg);
    background-repeat: no-repeat;
    background-size: contain;
  }
  @media (min-width: 991px) {
    background-color: transparent;
    border-radius: 4px;
    transition: background-color 0.3s;

    &:hover {
      background-color: $green;
    }
  }
}
</style>
