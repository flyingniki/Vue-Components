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
    <div class="delivery-type__contacts contacts">
      <div class="contacts__info">
        <p class="contacts__item">
          <span class="contacts__item-name">Адрес склада:&nbsp;</span>г. Москва,
          1-й Магистральный проезд, д. 8 с10
        </p>
        <p class="contacts__item">
          <span class="contacts__item-name">Режим работы:&nbsp;</span>в будние
          дни с 9:30 до 18:00
        </p>
        <p class="contacts__item">
          <span class="contacts__item-name">Телефон:&nbsp;</span>8 (495) xxx xx
          xx
        </p>
        <div class="contacts__footnote footnote">
          <img src="../assets/img/warning.png" alt="" class="footnote__img" />
          <p class="footnote__text">
            Подробности уточняются у менеджера при подтверждении заказа
          </p>
        </div>
      </div>
      <div class="contacts__card">
        <iframe
          class="contacts__card-frame"
          src="https://yandex.ru/map-widget/v1/?ll=37.526933%2C55.765403&mode=search&oid=124354844888&ol=biz&z=16.53"
          width="560"
          height="400"
          frameborder="1"
          allowfullscreen="true"
          style="position: relative"
        ></iframe>
      </div>
    </div>
  </div>
</template>

<script>
import DeliveryCard from "./DeliveryCard.vue";

export default {
  components: { DeliveryCard },
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

<style>
.delivery-type {
  box-sizing: border-box;
  width: 1032px;
  height: 513px;
  margin: 0 auto;
  padding: 30px 32px 53px;
  border: 1px solid #d5d5d5;
  border-radius: 15px;
}

.delivery-type__title {
  margin: 0;
  margin-bottom: 24px;
  font-size: 25px;
  font-weight: 500;
  line-height: 145%;
}

.delivery-type__block {
  display: flex;
  justify-content: space-between;
  column-gap: 16px;
  margin-bottom: 39px;
}

.contacts {
  display: flex;
  justify-content: space-between;
}

.contacts__item {
  margin: 0;
  margin-bottom: 4px;
  font-size: 16px;
  line-height: 135%;
  font-weight: 400;
}

.contacts__item-name {
  font-size: 16px;
  line-height: 145%;
  font-weight: 500;
}

.contacts__footnote {
  margin-top: 41px;
}

.footnote {
  display: flex;
  align-items: center;
}

.footnote__img {
  margin-right: 10px;
}

.footnote__text {
  margin: 0;
  font-size: 16px;
  line-height: 135%;
  font-weight: 500;
}

.contacts__card-frame {
  width: 100%;
  height: auto;
  border: none;
  border-radius: 15px;
}
</style>
