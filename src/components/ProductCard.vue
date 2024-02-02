<script>
import CardButton from "./ui/CardButton.vue";

export default {
  components: {
    CardButton,
  },
  props: {
    card: {
      type: Object,
      default: {
        id: 0,
        image: "../src/assets/img/Image.png",
        title: "Mobile SMARTS: Магазин 15 с МОТП",
        price: "12 300",
        currency: "₽",
        isAllowedForPurchase: true,
      },
      required: false,
    },
  },
  setup(props) {
    console.log(props);
  },
};
</script>

<template>
  <div class="product-card">
    <div class="product-card__picture card-picture">
      <img :src="card.image" alt="" class="card-picture__img" />
    </div>
    <div class="product-card__description card-description">
      <h2 class="card-description__title">{{ card.title }}</h2>
      <div class="card-description__footer">
        <p class="card-description__price">
          {{ card.price }} {{ card.currency }}
        </p>
        <CardButton :id="card.id" v-if="card.isAllowedForPurchase" />
      </div>
    </div>
  </div>
</template>

<style lang="sass" scoped>
.product-card {
  margin: 0 auto;
  width: 318px;
  border: 1px solid #d5d5d5;
  border-radius: 15px;
}

.product-card__picture {
  padding: 7px 28px 22px;
  background-color: #eeeef8;
  border-radius: 15px 15px 0 0;
}

.card-picture__img {
  width: 100%;
}

.product-card__description {
  box-sizing: border-box;
  height: 195px;
  border-radius: 0 0 15px 15px;
  padding: 32px;
}

.card-description__title {
  margin: 0;
  margin-bottom: 8px;
  max-width: 274px;
  height: 74px;
  font-weight: 500;
  font-size: 16px;
  line-height: 135%;
}

.card-description__footer {
  display: flex;
  justify-content: space-between;
  align-items: end;
}

.card-description__price {
  margin: 0;
  font-weight: 500;
  font-size: 24px;
  line-height: 130%;
}
</style>
