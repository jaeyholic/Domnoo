<template>
  <div>
    <Carousel :per-page='1' :autoplay='true' :paginationEnabled='false'>
      <slide v-for="(slide, index) in slides" :key="index">
        <div class="slider_bck"
          :style="{'background': `url(${slide.bck})`}">
          <div class="container slider-container">
            <div class="text">
              {{ slide.text }}
            </div>
            <div class="image">
              <img :src="slide.img" alt="">
            </div>
          </div>
        </div>
      </slide>
    </Carousel>
  </div>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";
import slideBG from "../../assets/images/slide_bck.jpg";
import slideBG2 from "../../assets/images/slide_bck2.jpg";
import pizzaOne from "../../assets/images/pizza_one.png";
import pizzaTwo from "../../assets/images/pizza_three.png";
export default {
  components: {
    Carousel,
    Slide
  },
  data() {
    return {
      slides: [
        {
          text: "20% OFF ON ALL PIZZAS",
          bck: slideBG,
          img: pizzaOne
        },
        {
          text: "BUY ONE, GET ONE FREE",
          bck: slideBG2,
          img: pizzaTwo
        }
      ]
    };
  }
};
</script>

<style scoped>
</style>