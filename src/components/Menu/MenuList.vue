<template>
  <ul class="menu">
    <li class="menu__item">
      <a class="menu__link" href="#">Work</a>
    </li>
    <li class="menu__item">
      <a class="menu__link" href="#">About</a>
    </li>
    <li class="menu__item">
      <a class="menu__link" href="#">Services</a>
    </li>
    <li class="menu__item">
      <a class="menu__link" href="#">Blog</a>
    </li>
    <li class="menu__item">
      <a class="menu__link" href="#">Contact</a>
    </li>
  </ul>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../../assets/scss/vars";

.menu {
  padding: 70px 0 30px;
  margin: 0;
  text-align: center;
  @media (min-width: 991px) {
    width: max-content;
    margin: 0 auto 50px;
    padding: 40px 0;
    border-top: 2px solid $grey2;
    border-bottom: 2px solid $grey2;
  }
}

.menu__item:not(:last-child) {
  margin-bottom: 20px;
}

.menu__link {
  display: block;
  padding: 5px 0;
  font-size: 22px;
  font-weight: 600;
  color: $grey4;
  text-transform: uppercase;
  transition: color .3s;

  &:hover {
    color: $green;
  }

  @media (min-width: 991px) {
    padding: 0;
    font-size: 18px;
  }
  @media (min-width: 1169px) {
    font-size: 16px;
  }
}

.menu--footer {
  display: none;
  @media (min-width: 991px) {
    display: flex;
    padding: 0;
    margin-bottom: 20px;
    border-top: none;
    border-bottom: none;
  }

  .menu__item {
    @media (min-width: 991px) {
      &:not(:last-child) {
        margin-bottom: 0;
        margin-right: 30px;
      }
    }
  }

  .menu__link {
    @media (min-width: 1169px) {
      font-size: 18px;
    }
  }
}
</style>
