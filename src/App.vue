<script>
import ProductCard from "./components/ProductCard.vue";
import CardsCarousel from "./components/CardsCarousel.vue";
import OrderForm from "./components/OrderForm.vue";

export default {
  components: {
    ProductCard,
    CardsCarousel,
    OrderForm
  },
};
</script>

<template>
  <div class="cart">
    <ProductCard />
    <CardsCarousel />
    <OrderForm />
  </div>
</template>

<style>
@import url("https://fonts.cdnfonts.com/css/montserrat");

* {
  font-family: "Montserrat", sans-serif;
}
</style>
