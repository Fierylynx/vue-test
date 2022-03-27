<template>
  <Header />
  <div class="main-content" id="body">
    <main>
      <Hero />
      <Services />
      <Quote />
      <Blog />
    </main>
  </div>
  <Footer />
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

.main-content {
  @media (min-width: 991px) {
    width: 100%;
    padding-left: 150px;
  }
}
</style>
