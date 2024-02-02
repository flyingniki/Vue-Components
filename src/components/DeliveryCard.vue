<script>
export default {
  props: {
    delivery: {
      type: Object,
      default: {
        id: 0,
        title: "Delivery title",
        info: "Delivery info",
        image: "../src/assets/img/self.png",
        isActive: false,
      },
    },
  },
};
</script>

<template>
  <div class="delivery-card" :class="{ active: delivery.isActive }">
    <h3 class="delivery-card__title">{{ delivery.title }}</h3>
    <p class="delivery-card__info">{{ delivery.info }}</p>
    <div class="delivery-card__selection">
      <img :src="delivery.image" alt="" class="delivery-card__img" />
      <button class="delivery-card__button">
        {{ delivery.isActive ? "Выбрано" : "Выбрать" }}
      </button>
    </div>
  </div>
</template>

<style lang="sass" scoped>
.delivery-card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  box-sizing: border-box;
  margin: 0 auto;
  width: 312px;
  height: 172px;
  border: 1px solid #47bfc7;
  border-radius: 15px;
  padding: 24px 12px 17px 16px;
}

.active {
  background-color: #edfcff;
}

.delivery-card__title {
  margin: 0;
  margin-bottom: 8px;
  font-size: 16px;
  line-height: 145%;
  font-weight: 500;
}

.delivery-card__info {
  margin: 0;
  padding: 0;
  margin-bottom: 36px;
}

.delivery-card__selection {
  display: flex;
  justify-content: space-between;
  align-items: end;
}

.delivery-card__button {
  color: #47bfc7;
  border: none;
  background-color: transparent;
  cursor: pointer;
}
</style>
