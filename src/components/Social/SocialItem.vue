<template>
  <li v-for="social in socials">
    <a href="#">
      <img :src="social.image" alt="" />
    </a>
  </li>
</template>

<script>
export default {
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

<style></style>
