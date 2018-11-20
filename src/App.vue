<template>
  <div>
    <Header />
    <Slider />
    <Menu />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header-Footer/Header";
import Footer from "./components/Header-Footer/Footer";
import Slider from "./components/Featured";
import Menu from "./components/Menu";
export default {
  components: {
    Header,
    Footer,
    Slider,
    Menu
  }
};
</script>

<style>
@import "./assets/style.css";
</style>
