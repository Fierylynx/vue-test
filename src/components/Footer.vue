<template>
  <footer class="footer section-padding section-bg">
    <div class="container">
      <div class="footer__wrapper">
        <SocialList :socials="socials"/>
        <div class="footer__content">
          <MenuList class="menu menu--footer" />
          <span class="footer__copy">
            (c) 2018 NAME. All rights reserved.
          </span>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import SocialList from "@/components/Social/SocialList";
import MenuList from "@/components/Menu/MenuList";
export default {
  components: {
    SocialList,
    MenuList,
  },
  data() {
    return {
      socials: [
        {
          image: require("@/assets/image/svg/facebook.svg"),
        },
        {
          image: require("@/assets/image/svg/twitter.svg"),
        },
        {
          image: require("@/assets/image/svg/instagram.svg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.footer {
  &.section-padding {
    padding: 70px 0;
  }
}

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
