<template>
  <div class="wrapper">
    <Header />
    <div class="main-content">
      <main>
        <Hero />
        <Services />
        <Quote />
        <Blog />
      </main>
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header";
import Hero from "@/components/Hero";
import Services from "@/components/Services/ServicesSection";
import Quote from "@/components/Quote";
import Blog from "@/components/Blog/BlogSection";
import Footer from "@/components/Footer";
export default {
  components: {
    Header,
    Hero,
    Services,
    Quote,
    Blog,
    Footer,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/reset";
@import "./assets/scss/global";

.wrapper {
  @media (min-width: 991px) {
    display: flex;
  }
}

.main-content {
    @media (min-width: 991px) {
      width: 100%;
  }
}
</style>
