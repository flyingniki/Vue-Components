<script>
export default {
  data() {
    return {
      hidden: false,
    };
  },
  methods: {
    popupClose() {
      this.hidden = true;
    },
  },
};
</script>

<template>
  <div class="popup-message" :class="{ hidden: hidden }">
    <h2 class="popup-message__title">Бесплатная доставка по Москве</h2>
    <div class="popup-message__content">
      <p class="popup-message__text">
        При покупке от 30 000 ₽ действует бесплатная доставка по Москве и
        Московской области.&nbsp;
        <a href="#" class="popup-message__link">Подробнее</a>
      </p>
      <a href="#" class="popup-message__close" @click.stop.prevent="popupClose">
        <img
          src="../assets/img/close-popup.png"
          alt=""
          class="popup-message__img"
        />
      </a>
    </div>
  </div>
</template>

<style lang="sass">
.hidden
  display: none

.popup-message
  width: 100%
  height: 80px
  margin: 0 auto

  &__content
    display: flex
    justify-content: center
    align-items: center
    background: linear-gradient(270deg, #60f8d6, #0b95ff)
    box-sizing: border-box
    padding: 27px auto

  &__title
    margin: 0

  &__text,
  &__link
    margin-right: 16px
    font-size: 20px
    font-weight: 500
    line-height: 135%
    
  &__close
    width: 32px
    height: 32px
</style>
