<template>
  <header class="header">
    <div class="header__wrapper">
      <a class="logo" href="#">
        <img src="../assets/image/svg/logo.svg" alt="logo" />
      </a>
      <Menu />
    </div>
  </header>
</template>

<script>
import Menu from "@/components/Menu/Menu";
export default {
  components: {
    Menu,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/vars";

.logo {
  position: relative;
  z-index: 100;

  @media (min-width: 991px) {
    margin: 40px 0 55px;
  }
}

.header {
  position: fixed;
  width: 100%;
  padding: 10px;
  background-color: $black;
  z-index: 120;

  @media (min-width: 991px) {
    max-width: 150px;
    width: 100%;
    padding: 0;
  }
}

.header__wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;

  @media (min-width: 991px) {
    flex-direction: column;
  }
}
</style>
