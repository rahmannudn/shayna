<template>
  <div class="home">
    <HeaderShayna />
    <HeroShayna />
    <BannerShayna />
    <InstaShayna />
    <PartnerShayna />
    <FooterShayna />
  </div>
</template>

<script>
import HeaderShayna from "../components/HeaderShayna.vue";
import HeroShayna from "../components/HeroShayna.vue";
import BannerShayna from "../components/BannerShayna.vue";
import InstaShayna from "../components/InstaShayna.vue";
import PartnerShayna from "../components/PartnerShayna.vue";
import FooterShayna from "../components/FooterShayna.vue";

export default {
  name: "HomeView",
  components: {
    HeaderShayna,
    HeroShayna,
    BannerShayna,
    InstaShayna,
    PartnerShayna,
    FooterShayna,
  },
};
</script>

<style>
.set-bg {
  width: 100%;
  height: 500px;
}
.banner-info {
  margin-top: 120px;
}
</style>
