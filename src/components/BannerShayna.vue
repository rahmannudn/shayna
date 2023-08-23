<template>
  <!-- Women Banner Section Begin -->
  <section class="women-banner spad">
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-12 mt-5">
          <Carousel
            class="product-slider"
            items-to-show="3"
            :autoplay="1500"
            :transition="500"
          >
            <Slide class="product-item">
              <div class="pi-pic">
                <img src="img/mickey1.jpg" alt="" />
                <ul>
                  <li class="w-icon active">
                    <router-link to="/product"
                      ><i class="icon_bag_alt"></i
                    ></router-link>
                  </li>
                  <li class="quick-view">
                    <router-link to="product.html">+ Quick View</router-link>
                  </li>
                </ul>
              </div>
              <div class="pi-text">
                <div class="catagory-name">Coat</div>
                <router-link to="/product">
                  <h5>Mickey Baggy</h5>
                </router-link>
                <div class="product-price">
                  $14.00
                  <span>$35.00</span>
                </div>
              </div>
            </Slide>
            <Slide class="product-item">
              <div class="pi-pic">
                <img src="img/products/women-2.jpg" alt="" />
                <ul>
                  <li class="w-icon active">
                    <router-link to="/product"
                      ><i class="icon_bag_alt"></i
                    ></router-link>
                  </li>
                  <li class="quick-view">
                    <router-link to="/product">+ Quick View</router-link>
                  </li>
                </ul>
              </div>
              <div class="pi-text">
                <div class="catagory-name">Shoes</div>
                <router-link to="/product">
                  <h5>Guangzhou sweater</h5>
                </router-link>
                <div class="product-price">$13.00</div>
              </div>
            </Slide>
            <Slide class="product-item">
              <div class="pi-pic">
                <img src="img/products/women-3.jpg" alt="" />
                <ul>
                  <li class="w-icon active">
                    <router-link to="/product"
                      ><i class="icon_bag_alt"></i
                    ></router-link>
                  </li>
                  <li class="quick-view">
                    <router-link to="/product">+ Quick View</router-link>
                  </li>
                </ul>
              </div>
              <div class="pi-text">
                <div class="catagory-name">Towel</div>
                <router-link to="/product">
                  <h5>Pure Pineapple</h5>
                </router-link>
                <div class="product-price">$34.00</div>
              </div>
            </Slide>
            <Slide class="product-item">
              <div class="pi-pic">
                <img src="img/products/women-4.jpg" alt="" />
                <ul>
                  <li class="w-icon active">
                    <router-link to="/product"
                      ><i class="icon_bag_alt"></i
                    ></router-link>
                  </li>
                  <li class="quick-view">
                    <router-link to="/product">+ Quick View</router-link>
                  </li>
                  <li class="w-icon">
                    <router-link to="/product"
                      ><i class="fa fa-random"></i
                    ></router-link>
                  </li>
                </ul>
              </div>
              <div class="pi-text">
                <div class="catagory-name">Towel</div>
                <router-link to="/product">
                  <h5>Converse Shoes</h5>
                </router-link>
                <div class="product-price">$34.00</div>
              </div>
            </Slide>
            <template #addons>
              <Pagination />
            </template>
          </Carousel>
        </div>
      </div>
    </div>
  </section>
  <!-- Women Banner Section End -->
</template>

<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination } from "vue3-carousel";

export default {
  name: "BannerShayna",
  components: {
    Carousel,
    Slide,
    Pagination,
  },
};
</script>

<style scoped>
.product-item {
  display: flex;
  flex-direction: column;
}

.pi-pic img {
  width: 380px;
  height: 380px;
}
</style>
