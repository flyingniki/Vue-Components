<script>
import ProductCard from "./components/ProductCard.vue";
import CardsCarousel from "./components/CardsCarousel.vue";
import Form from "./components/Form.vue";

export default {
  components: {
    ProductCard,
    CardsCarousel,
    Form
  },
};
</script>

<template>
  <div class="cart">
    <ProductCard />
    <CardsCarousel />
    <Form />
  </div>
</template>

<style>
@import url("https://fonts.cdnfonts.com/css/montserrat");

* {
  font-family: "Montserrat", sans-serif;
}
</style>
