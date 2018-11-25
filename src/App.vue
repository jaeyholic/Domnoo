<template>
  <div>
    <Header />
    <Slider />
    <Menu />
    <CTA/>
    <Newsletter />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header-Footer/Header";
import Footer from "./components/Header-Footer/Footer";
import Slider from "./components/Featured";
import Menu from "./components/Menu";
import CTA from "./components/CTA";
import Newsletter from "./components/Newsletter";
export default {
  components: {
    Header,
    Footer,
    Slider,
    Menu,
    CTA,
    Newsletter
  }
};
</script>

<style>
@import "./assets/style.css";
</style>
