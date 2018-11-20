<template>
  <header>
    <div class="container clear">
      <div class="logo">
        <img :src="logoIcon" alt="">
      </div>
      <div class="nav">
        <img :src="MenuIcon" @click="showSidePanel = !showSidePanel">
      </div>
      <md-drawer
        :md-active.sync='showSidePanel'
        class="md-right side-drawer"
      />
    </div>
  </header>
</template>

<script>
import Logo from "../../assets/images/logo.png";
import Menu from "../../assets/images/menu.png";
export default {
  data() {
    return {
      logoIcon: Logo,
      MenuIcon: Menu,
      showSidePanel: false
    };
  }
};
</script>

<style scoped>
</style>