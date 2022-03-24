<template>
  <footer class="footer section-padding section-bg">
    <div class="container">
      <div class="footer__wrapper">
        <Social />
        <div class="footer__content">
          <Menu />
          <span class="footer__copy">
            (c) 2018 NAME. All rights reserved.
          </span>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Social from "@/components/Social/SocialList";
import Menu from "@/components/Menu/MenuList";
export default {
  components: {
    Social,
    Menu,
  },
  
};
</script>

<style lang="scss" scoped>

.footer__wrapper {
    @media (min-width: 991px) {
      display: flex;
      flex-direction: row-reverse;
      align-items: center;
      justify-content: space-between;
  }
}

.footer__copy {
  display: block;
  font-size: 16px;
  text-align: center;
    @media (min-width: 991px) {
    text-align: left;
  }
}
</style>
