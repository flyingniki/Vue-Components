<script>
import ProductCard from "./ProductCard.vue";

export default {
  components: {
    ProductCard,
  },
  data() {
    return {
      cards: [
        {
          id: 1,
          image: "../src/assets/img/Image.png",
          title: "Mobile SMARTS: Магазин 15 с МОТП",
          price: "12 300",
          currency: "₽",
          isAllowedForPurchase: true,
        },
        {
          id: 2,
          image: "../src/assets/img/Image.png",
          title: "Mobile SMARTS: Магазин 15 с МОТП",
          price: "12 300",
          currency: "₽",
          isAllowedForPurchase: false,
        },
        {
          id: 3,
          image: "../src/assets/img/Image.png",
          title: "Mobile SMARTS: Магазин 15 с МОТП",
          price: "12 300",
          currency: "₽",
          isAllowedForPurchase: true,
        },
        {
          id: 4,
          image: "../src/assets/img/Image.png",
          title: "Mobile SMARTS: Магазин 15 с МОТП",
          price: "12 300",
          currency: "₽",
          isAllowedForPurchase: false,
        },
        {
          id: 5,
          image: "../src/assets/img/Image.png",
          title: "Mobile SMARTS: Магазин 15 с МОТП",
          price: "12 300",
          currency: "₽",
          isAllowedForPurchase: true,
        },
      ],
    };
  },
};
</script>

<template>
  <div class="cards-seen">
    <div class="cards-seen__info">
      <h2 class="cards-seen__title">Вы смотрели</h2>
    </div>
    <div class="cards-seen__carousel">
      <ProductCard v-for="card in cards" :id="card.id" :card="card" />
    </div>
  </div>
</template>

<style lang="sass" scoped>
.cards-seen__title
  margin: 0
  font-weight: 500
  font-size: 25px
  line-height: 145%
.cards-seen__carousel
  display: flex
  column-gap: 8px
</style>
