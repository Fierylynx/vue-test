<template>
  <header class="header">
    <div class="header__wrapper">
      <a class="logo" href="#">
        <img src="../assets/image/svg/logo.svg" alt="" />
      </a>
      <Menu />
    </div>
  </header>
</template>

<script>
import Menu from "@/components/Menu";
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
    padding: 40px 0 55px;
  }
}

.header {
  position: relative;
  padding: 10px;
  background-color: $black;
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
