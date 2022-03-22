<template>
  <button
    class="burger"
    v-on:click="navOpen = !navOpen"
    v-bind:class="{ active: navOpen }"
  >
    <span class="top"></span>
    <span class="mid"></span>
    <span class="bottom"></span>
  </button>
  <!-- <transition name="translateX"> -->
  <nav v-show="navOpen">
    <div class="menu">
      <ul class="menu__list">
        <li class="menu__item"><a href="">Work</a></li>
        <li class="menu__item"><a href="">About</a></li>
        <li class="menu__item"><a href="">Services</a></li>
        <li class="menu__item"><a href="">Blog</a></li>
        <li class="menu__item"><a href="">Contact</a></li>
      </ul>
    </div>
  </nav>
  <!-- </transition> -->
  <!-- <button
      class="burger"
      type="button"
      @click="navOpen = !navOpen"
      v-bind:class="{ active: navOpen }"
    >
      <span></span>
      <span></span>
      <span></span>
    </button>
  <nav class="menu" v-show="navOpen">
    <ul class="menu__list">
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
  </nav> -->
</template>

<script>
export default {
  data() {
    return {
      navOpen: false,
    };
  },
};
</script>

<style lang="scss">
nav {
  width: 100%;
  height: 100vh;
  background: grey;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 99;
  &.active {
    transition: display 0.5s;
  }
}

.burger {
  display: block;
  width: 45px;
  height: 30px;
  background-color: transparent;
  border: none;
  position: relative;
  z-index: 100;

  span {
    display: block;
    width: 45px;
    height: 4px;
    margin: auto;
    background-color: rgba(255, 255, 255, 0.5);
    border-radius: 2px;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    transition: all 0.4s ease;

    &.top {
      transform: translateY(-13px);
    }

    &.bottom {
      transform: translateY(13px);
    }
  }
  &.active {
    .top {
      transform: rotate(-45deg);
    }
    .mid {
      transform: translateX(-20px) rotate(360deg);
      opacity: 0;
    }
    .bottom {
      transform: rotate(45deg);
    }
  }
}

.menu {
  padding-top: 50px;

  &__list {
    padding-top: 50px;
    list-style: none;
    padding: 0;
    margin: 0;
  }

  &__item {
    a {
      text-decoration: none;
      line-height: 1.6em;
      font-size: 1.6em;
      padding: 0.5em;
      display: block;
      color: white;
      transition: 0.4s ease;

      &:hover {
        background: lightgrey;
        color: dimgrey;
      }
    }
  }
}
</style>
