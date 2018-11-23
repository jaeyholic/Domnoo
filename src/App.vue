<template>
  <div>
    <Header />
    <Slider />
    <Menu />
    <CTA/>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header-Footer/Header";
import Footer from "./components/Header-Footer/Footer";
import Slider from "./components/Featured";
import Menu from "./components/Menu";
import CTA from "./components/CTA";
export default {
  components: {
    Header,
    Footer,
    Slider,
    Menu,
    CTA
  }
};
</script>

<style>
@import "./assets/style.css";
</style>
