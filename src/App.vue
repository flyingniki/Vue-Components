<script>
import ProductCard from "./components/products/ProductCard.vue";
import CardsCarousel from "./components/products/CardsCarousel.vue";
import OrderForm from "./components/customer/OrderForm.vue";
import DeliveryCard from "./components/delivery/DeliveryCard.vue";
import DeliveryType from "./components/delivery/DeliveryType.vue";
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
    <CardsCarousel />
    <div class="separator"></div>
    <OrderForm />
    <div class="separator"></div>
    <DeliveryType />
    <div class="separator"></div>
    <PopupMessage />
  </div>
</template>

<style lang="sass">
@import url("https://fonts.cdnfonts.com/css/montserrat")

*
  font-family: "Montserrat", sans-serif
  color: #141212
  font-weight: 400
  
.separator
  height: 20px
</style>
