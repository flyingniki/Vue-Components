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
    <div class="delivery-card__description">
      <h3 class="delivery-card__title">{{ delivery.title }}</h3>
      <p class="delivery-card__info">{{ delivery.info }}</p>
    </div>
    <div class="delivery-card__selection">
      <img :src="delivery.image" alt="" class="delivery-card__img" />
      <button class="delivery-card__button">
        {{ delivery.isActive ? "Выбрано" : "Выбрать" }}
      </button>
    </div>
  </div>
</template>

<style lang="sass">
.active
  background-color: #edfcff

.delivery-card
  display: flex
  flex-direction: column
  justify-content: space-between
  box-sizing: border-box
  margin: 0 auto
  width: 312px
  height: 172px
  border: 1px solid #47bfc7
  border-radius: 15px
  padding: 24px 12px 17px 16px

  &__title
    margin: 0
    margin-bottom: 8px
    font-size: 16px
    line-height: 145%
    font-weight: 600

  &__info
    margin: 0
    padding: 0

  &__selection
    display: flex
    justify-content: space-between
    align-items: end

  &__button
    color: #47bfc7
    font-size: 16px
    font-weight: 500
    border: none
    background-color: transparent
    cursor: pointer
</style>
