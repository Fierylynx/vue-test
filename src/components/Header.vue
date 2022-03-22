<template>
  <header class="header">
    <div class="header__wrapper">
      <a class="logo" href="#">
        <img src="../assets/svg/logo.svg" alt="" />
      </a>
      <Menu />
      <button class="header__search"></button>
      <input class="header__input" type="text" />
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
.logo {
  position: relative;
  z-index: 100;
}

.header {
  padding: 10px;
  background-color: #282d31;
}

.header__wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header__input {
  display: none;
}

.header__search {
  position: relative;
  width: 28px;
  height: 28px;
  background-image: url(../assets/svg/loupe.svg);
  background-size: cover;
  background-color: transparent;
  border: none;
  z-index: 100;
}
</style>
