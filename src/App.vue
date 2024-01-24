<script>
import ProductCard from "./components/ProductCard.vue";
import CardsCarousel from "./components/CardsCarousel.vue";

export default {
  components: {
    ProductCard,
    CardsCarousel,
  },
};
</script>

<template>
  <div class="cart">
    <ProductCard />
    <CardsCarousel />
  </div>
</template>

<style>
@import url("https://fonts.cdnfonts.com/css/montserrat");

* {
  font-family: "Montserrat", sans-serif;
}
</style>
