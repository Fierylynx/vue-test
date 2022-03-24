<template>
  <div class="menu">
    <ul class="menu__list">
      <li class="menu__item"><a href="">Work</a></li>
      <li class="menu__item"><a href="">About</a></li>
      <li class="menu__item"><a href="">Services</a></li>
      <li class="menu__item"><a href="">Blog</a></li>
      <li class="menu__item"><a href="">Contact</a></li>
    </ul>
  </div>
</template>

<script>
export default {
};
</script>

<style lang="scss">
@import "../../assets/scss/vars";

.menu {
  padding: 70px 0 30px;

  &__list {
    padding-top: 50px;
    padding: 0;
    margin: 0;
    text-align: center;
  }

  &__item:not(:last-child) {
    margin-bottom: 20px;
  }

  & a {
    display: block;
    padding: 5px 0;
    font-size: 22px;
    font-weight: 600;
    color: $grey3;
    text-transform: uppercase;
  }
  @media (min-width: 991px) {
    & a {
      padding: 0;
      font-size: 24px;
    }
  }
}

// .menu--footer {
//   display: none;
//   @media (min-width: 991px) {
//     display: block;
//     padding: 0;
//   }
//   .menu__list {
//     @media (min-width: 991px) {
//       display: flex;
//     }
//   }

//   .menu__item {
//     @media (min-width: 991px) {
//       &:not(:last-child) {
//         margin-bottom: 0;
//         margin-right: 30px;
//       }
//     }
//   }
// }
</style>
