<script>
export default {};
</script>

<template>
  <div class="contacts">
    <div class="contacts__info">
      <p class="contacts__item">
        <span class="contacts__item-name">Адрес склада:&nbsp;</span>г. Москва,
        1-й Магистральный проезд, д. 8 с10
      </p>
      <p class="contacts__item">
        <span class="contacts__item-name">Режим работы:&nbsp;</span>в будние дни
        с 9:30 до 18:00
      </p>
      <p class="contacts__item">
        <span class="contacts__item-name">Телефон:&nbsp;</span>8 (495) xxx xx xx
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
</template>

<style lang="sass">
.contacts
  display: flex
  justify-content: space-between

  &__item
    margin: 0
    margin-bottom: 4px
    font-size: 16px
    line-height: 135%
    font-weight: 400

    &-name
      font-size: 16px
      line-height: 145%
      font-weight: 500

  &__footnote
    margin-top: 41px
    display: flex
    align-items: center

  &__card-frame
    width: 100%
    height: auto
    border: none
    border-radius: 15px

.footnote
  &__img
    margin-right: 10px

  &__text
    margin: 0
    font-size: 16px
    line-height: 135%
    font-weight: 500
</style>
