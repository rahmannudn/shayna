<template>
  <div class="home">
    <HeaderShayna />
    <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="breadcrumb-text product-more text-left">
              <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
              <span>Detail</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="row">
              <div class="col-lg-6">
                <div class="product-pic-zoom">
                  <img
                    class="product-big-img"
                    v-bind:src="`img/${productImages[currentSlide]}`"
                  />
                </div>
                <div class="product-thumbs">
                  <Carousel id="thumbnails" :items-to-show="3" ref="carousel">
                    <Slide v-for="(image, index) in productImages" :key="image">
                      <div
                        class="pt carousel__item"
                        v-bind:class="index === currentSlide ? 'active' : ''"
                        @click="changeSlide(index)"
                      >
                        <img :src="`img/${image}`" />
                      </div>
                    </Slide>
                  </Carousel>
                </div>
              </div>
              <div class="col-lg-6">
                <div class="product-details text-left">
                  <div class="pd-title">
                    <span>oranges</span>
                    <h3>Pure Pineapple</h3>
                  </div>
                  <div class="pd-desc">
                    <p>
                      Lorem ipsum dolor sit amet consectetur adipisicing elit.
                      Corporis, error officia. Rem aperiam laborum voluptatum
                      vel, pariatur modi hic provident eum iure natus quos non a
                      sequi, id accusantium! Autem.
                    </p>
                    <p>
                      Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                      Quam possimus quisquam animi, commodi, nihil voluptate
                      nostrum neque architecto illo officiis doloremque et
                      corrupti cupiditate voluptatibus error illum. Commodi
                      expedita animi nulla aspernatur. Id asperiores blanditiis,
                      omnis repudiandae iste inventore cum, quam sint molestiae
                      accusamus voluptates ex tempora illum sit perspiciatis.
                      Nostrum dolor tenetur amet, illo natus magni veniam quia
                      sit nihil dolores. Commodi ratione distinctio harum
                      voluptatum velit facilis voluptas animi non laudantium, id
                      dolorem atque perferendis enim ducimus? A exercitationem
                      recusandae aliquam quod. Itaque inventore obcaecati, unde
                      quam impedit praesentium veritatis quis beatae ea atque
                      perferendis voluptates velit architecto?
                    </p>
                    <h4>$495.00</h4>
                  </div>
                  <div class="quantity">
                    <router-link
                      to="shopping-cart.html"
                      class="primary-btn pd-cart"
                      >Add To Cart</router-link
                    >
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Product Shop Section End -->
    <RelatedProductShayna />
    <FooterShayna />
  </div>
</template>

<script>
import HeaderShayna from "@/components/HeaderShayna.vue";
import FooterShayna from "@/components/FooterShayna.vue";
import RelatedProductShayna from "@/components/RelatedProductShayna.vue";
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide } from "vue3-carousel";
export default {
  name: "ProductView",
  components: {
    HeaderShayna,
    FooterShayna,
    Carousel,
    Slide,
    RelatedProductShayna,
  },
  data() {
    return {
      productImages: [
        "mickey1.jpg",
        "mickey2.jpg",
        "mickey3.jpg",
        "mickey4.jpg",
      ],
      currentSlide: 0,
    };
  },
  methods: {
    changeSlide(slideIndex) {
      this.currentSlide = slideIndex;
    },
    notify(message) {
      alert(message);
    },
  },
};
</script>

<style>
.product-thumbs .pt {
  margin-right: 10px;
}
</style>
