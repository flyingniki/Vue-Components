<script>
export default {};
</script>

<template>
  <div class="address-form-container">
    <form class="address-form" action="#" method="post">
      <h2 class="address-form__title">Укажите адрес доставки</h2>
      <ul class="address-form__list">
        <li class="address-form__item text-field">
          <label class="text-field__label" for="city"></label>
          <input
            class="text-field__input"
            type="text"
            name="city"
            id="city"
            placeholder="Населенный пункт"
          />
        </li>
        <li class="address-form__item text-field">
          <label class="text-field__label" for="street"></label>
          <input
            class="text-field__input"
            type="text"
            name="street"
            id="street"
            placeholder="Улица*"
          />
        </li>
        <li class="address-form__item text-field">
          <label class="text-field__label" for="building"></label>
          <input
            class="text-field__input"
            type="text"
            name="building"
            id="building"
            placeholder="Дом*"
          />
        </li>
        <li class="address-form__item text-field">
          <label class="text-field__label" for="apartment"></label>
          <input
            class="text-field__input"
            type="text"
            name="apartment"
            id="apartment"
            placeholder="Квартира"
          />
        </li>
        <li class="address-form__item text-field">
          <label class="text-field__label" for="entrance"></label>
          <input
            class="text-field__input"
            type="text"
            name="entrance"
            id="entrance"
            placeholder="Подъезд"
          />
        </li>
        <li class="address-form__item text-field">
          <label class="text-field__label" for="floor"></label>
          <input
            class="text-field__input"
            type="text"
            name="floor"
            id="floor"
            placeholder="Этаж"
          />
        </li>
        <li class="address-form__item text-field">
          <label class="text-field__label" for="comment"></label>
          <input
            class="text-field__input"
            type="text"
            name="comment"
            id="comment"
            placeholder="Комментарий"
          />
        </li>
      </ul>
    </form>
  </div>
</template>

<style lang="sass">
.address-form
  &-container
    width: 968px

  &__title
    margin: 0
    margin-bottom: 16px
    font-size: 20px
    font-weight: 600

  &__list
    list-style: none
    margin: 0
    padding: 0
    display: flex
    flex-wrap: wrap
    gap: 16px
    justify-content: space-between

  &__item
    width: 476px

    &:nth-child(3)
      width: 230px

    &:nth-child(4)
      width: 230px

    &:nth-child(5)
      width: 230px

    &:nth-child(6)
      width: 230px

    &:nth-child(7)
      width: 968px

.text-field
  &__input
    box-sizing: border-box
    background-color: #edfcff
    width: 100%
    height: 46px
    border: 1px solid #47bfc7
    border-radius: 10px
    padding: 13px 16px
    color: #47bfc7

    &::placeholder
      color: #47bfc7
</style>
