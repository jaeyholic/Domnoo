<template>
  <footer>
    <div class="container">
      <div>
        <img :src="logoIcon" alt="">
        <div class="contact">
          <div>Call us</div>
          <div>555.555.555</div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Logo from "../../assets/images/logo.png";
export default {
  data() {
    return {
      logoIcon: Logo
    };
  }
};
</script>

<style scoped>
</style>