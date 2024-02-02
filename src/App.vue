<script>
import ProductCard from "./components/ProductCard.vue";
import CardsCarousel from "./components/CardsCarousel.vue";
import OrderForm from "./components/OrderForm.vue";
import DeliveryCard from "./components/DeliveryCard.vue";
import DeliveryType from "./components/DeliveryType.vue";
import PopupMessage from "./components/PopupMessage.vue";

export default {
  components: {
    ProductCard,
    CardsCarousel,
    OrderForm,
    DeliveryCard,
    DeliveryType,
    PopupMessage,
  },
};
</script>

<template>
  <div class="cart">
    <ProductCard />
    <div class="separator"></div>
    <CardsCarousel />
    <div class="separator"></div>
    <OrderForm />
    <div class="separator"></div>
    <DeliveryCard />
    <div class="separator"></div>
    <DeliveryType />
    <div class="separator"></div>
    <PopupMessage />
  </div>
</template>

<style lang="sass" scoped>
@import url("https://fonts.cdnfonts.com/css/montserrat")

*
  font-family: "Montserrat", sans-serif
  color: #141212
  font-weight: 400
.separator
  height: 20px
</style>
