<template>
  <button
    class="burger"
    @click="navOpen = !navOpen"
    v-bind:class="{ active: navOpen }"
  >
    <span></span>
    <span></span>
    <span></span>
  </button>
  <nav v-show="navOpen">
    <MenuList />
    <form class="menu__form">
      <input
        class="menu__input"
        type="text"
        v-bind:value="inputValue"
        v-show="inputVisibility"
      />
      <button
        class="menu__search"
        @click.prevent="inputVisibility = !inputVisibility"
        type="button"
      ></button>
    </form>
  </nav>
</template>

<script>
import MenuList from "@/components/Menu/MenuList";
export default {
  components: {
    MenuList,
  },
  data() {
    return {
      navOpen: false,
      inputValue: "",
      inputVisibility: true,
    };
  },
  // props: {
  //   footerMenu: true,
  // },
  methods: {
    startSearch() {
      console.log("Начинаю поиск", this.inputValue);
    },
  },
};
</script>

<style lang="scss">
@import "../assets/scss/vars";

nav {
  position: fixed;
  top: 0;
  left: 0;
  padding: 20px;
  width: 100%;
  height: 100vh;
  background-color: $black;
  z-index: 99;
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
    margin: auto;
    width: 45px;
    height: 4px;
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

.menu__form {
  display: flex;
  align-items: center;
  justify-content: center;
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
    // display: none;
  }
}

.menu__search {
  position: relative;
  padding: 2px;
  width: 44px;
  height: 44px;
  background-color: $grey3;
  border: none;
  border-radius: 0 4px 4px 0;
  z-index: 100;

  &::after {
    position: absolute;
    top: 7px;
    left: 6px;
    content: "";
    width: 30px;
    height: 30px;
    background-image: url(../assets/image/svg/loupe.svg);
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
