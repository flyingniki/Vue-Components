<script>
import DeliveryCard from "./DeliveryCard.vue";
import DeliveryCourier from "./DeliveryCourier.vue";
import DeliveryPickup from "./DeliveryPickup.vue";
import DeliveryRegionVue from "./DeliveryRegion.vue";

export default {
  components: {
    DeliveryCard,
    DeliveryPickup,
    DeliveryCourier,
    DeliveryRegionVue,
  },
  data() {
    return {
      deliveries: [
        {
          id: 0,
          title: "Самовывоз",
          info: "Бесплатно",
          image: "../src/assets/img/self.png",
          isActive: true,
        },
        {
          id: 1,
          title: "Курьером по Москве и МО",
          info: "Бесплатно при заказе от 30 000 ₽ ",
          image: "../src/assets/img/self.png",
          isActive: false,
        },
        {
          id: 2,
          title: "Доставка по регионам РФ",
          info: "Стоимость рассчитывается на этапе подтверждения заказа",
          image: "../src/assets/img/self.png",
          isActive: false,
        },
      ],
    };
  },
  methods: {
    btnSelect(id) {
      this.deliveries.forEach((delivery) => {
        delivery.isActive = false;
      });
      this.deliveries[id].isActive = true;
    },
  },
};
</script>

<template>
  <div class="delivery-type">
    <h2 class="delivery-type__title">Способ доставки</h2>
    <div class="delivery-type__block">
      <DeliveryCard
        v-for="delivery in deliveries"
        :id="delivery.id"
        :delivery="delivery"
        @click="btnSelect(delivery.id)"
      />
    </div>
    <DeliveryPickup v-show="show" />
    <DeliveryCourier v-show="show" />
    <DeliveryRegionVue v-show="show" />
  </div>
</template>

<style lang="sass">
.delivery-type
  box-sizing: border-box
  width: 1032px
  margin: 0 auto
  padding: 32px
  border: 1px solid #d5d5d5
  border-radius: 15px

.delivery-type__title
  margin: 0
  margin-bottom: 24px
  font-size: 25px
  font-weight: 500
  line-height: 145%

.delivery-type__block
  display: flex
  justify-content: space-between
  column-gap: 16px
  margin-bottom: 39px
</style>
