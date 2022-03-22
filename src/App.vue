<template>
  <Header />
  <main>
    <Hero />
    <Services />
    <Quote />
    <Blog />
    <Footer />
  </main>
</template>

<script>
import Header from "@/components/Header";
import Hero from "@/components/Hero";
import Services from "@/components/Services";
import Quote from "@/components/Quote";
import Blog from "@/components/Blog";
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
html {
  box-sizing: border-box;
}

*,
*::after,
*::before {
  box-sizing: inherit;
}

ul,
ol {
  padding: 0;
}

body,
h1,
h2,
h3,
h4,
h5,
h6,
p,
ul,
ol,
li,
figure,
figcaption,
blockquote,
dl,
dd {
  margin: 0;
}

ul {
  list-style: none;
}

img {
  max-width: 100%;
  display: block;
}

input,
button,
textarea,
select {
  font: inherit;
  letter-spacing: inherit;
}

button {
  cursor: pointer;
}

a {
  color: inherit;
  text-decoration: none;
}




body {
  font-family: 'Poppins', sans-serif;
  font-size: 18px;
  line-height: 1.7;
  font-weight: 300;
  color: #5A5F65;
}

.section-padding {
  padding: 50px 0;
}

.button {
  max-width: 160px;
  width: 100%;
  font-size: 20px;
  line-height: 2;
  font-weight: 600;
  color: #FFFFFF;
  background-color: #4CB481;
  border: none;
  border-radius: 100px;
  text-transform: uppercase;
}

.top-element {
  position: relative;
  padding-top: 20px;
  &::before {
    position: absolute;
    top: 0;
    left: 0;
    content: '';
    width: 45px;
    height: 4px;
    background-color: #4CB481;
    border-radius: 2px;

  }
}
</style>
