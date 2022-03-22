<template>
  <footer class="footer section-padding">
    <ul class="social">
      <li>
        <a href="#">
          <img src="../assets/svg/facebook.svg" alt="" />
        </a>
      </li>
      <li>
        <a href="#">
          <img src="../assets/svg/twitter.svg" alt="" />
        </a>
      </li>
      <li>
        <a href="#">
          <img src="../assets/svg/instagram.svg" alt="" />
        </a>
      </li>
    </ul>
    <span class="footer__copy">
      (c) 2018 NAME. All rights reserved.
    </span>
  </footer>
</template>

<script>
export default {};
</script>

<style lang='scss'>
.footer {
  background-color: #282d31;
}

.social {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;

  li:not(:last-child) {
    margin-right: 30px;
  }
}

.footer__copy {
  display: block;
  font-size: 16px;
  text-align: center;
}
</style>
