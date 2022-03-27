<template>
  <button
    class="burger"
    type="button"
    @click="navOpen = !navOpen"
    v-bind:class="{ active: navOpen }"
  >
    <span></span>
    <span></span>
    <span></span>
  </button>
  <nav v-show="navOpen">
    <MenuList />
    <MenuForm />
  </nav>
</template>

<script>
import MenuList from "@/components/Menu/MenuList";
import MenuForm from "@/components/Form/MenuForm";
export default {
  components: {
    MenuList,
    MenuForm,
  },
  data() {
    return {
      navOpen: false,
    };
  },
};
</script>

<style lang="scss">
@import "../../assets/scss/vars";

nav {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 99;
  width: 100%;
  height: 100vh;
  padding: 20px;
  background-color: $black;
  overflow: scroll;
  @media (min-width: 991px) {
    position: relative;
    display: block !important;
    padding: 0;
  }
}

.burger {
  position: relative;
  display: block;
  width: 45px;
  height: 30px;
  background-color: transparent;
  border: none;
  z-index: 100;

  span {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    display: block;
    width: 45px;
    height: 4px;
    margin: auto;
    background-color: $grey3;
    border-radius: 2px;
    transition: transform 0.4s ease;

    &:nth-child(2) {
      transform: translateY(-13px);
    }

    &:nth-child(3) {
      transform: translateY(13px);
    }
  }
  &.active {
    span {
      transform: rotate(-45deg);
    }
    span:nth-child(1) {
      transform: translateX(-20px) rotate(360deg);
      opacity: 0;
    }
    span:nth-child(2) {
      transform: rotate(45deg);
    }
  }
  @media (min-width: 991px) {
    display: none;
  }
}
</style>
