<template>
  <!-- Hero Section Begin -->
  <section class="hero-section">
    <Carousel :items-to-show="1">
      <Slide v-for="(src, index) in imageSoruces" :key="index">
        <div
          class="single-hero-items set-bg"
          :style="`background-image: url(./img/${src}) `"
        >
          <div class="container">
            <div class="row">
              <div class="col-lg-5 banner-info">
                <span>Bag,kids</span>
                <h1>Black friday</h1>
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed
                  do eiusmod tempor incididunt ut labore et dolore
                </p>
                <a href="#" class="primary-btn">Shop Now</a>
              </div>
            </div>
          </div>
        </div>
      </Slide>

      <template #addons>
        <Navigation />
        <Pagination />
      </template>
    </Carousel>
  </section>
  <!-- Hero Section End -->
</template>

<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

export default {
  name: "HeroShayna",
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  data() {
    return {
      imageSoruces: ["hero-1.jpg", "hero-2.jpg", "hero-3.jpg"],
    };
  },
};
</script>
